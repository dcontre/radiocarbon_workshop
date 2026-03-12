oxcalSimulate_cc <- function (c_date, std, names = 1:length(c_date), cc = "IntCal20")
{
  cc <- paste("Curve(\"", cc, "\", \"", tolower(cc), ".14c\");", collapse = "\n", sep = "")
  oxcal_script <- paste(cc,
                        R_Simulate(c_date, std, names), collapse = "\n")
  result_file <- executeOxcalScript(oxcal_script)
  result <- readOxcalOutput(result_file)
  RVA <- parseOxcalOutput(result, only.R_Date = F)
  RVA
}
