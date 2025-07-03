# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Nonlinear mixed-effects model fit by maximum likelihood Use nlme With (In) R Software
install.packages("nlme")
library("nlme")
nlme = read.csv("https://raw.githubusercontent.com/timbulwidodostp/nlme/main/nlme/nlme.csv",sep = ";")
# Estimation Nonlinear mixed-effects model fit by maximum likelihood Use nlme With (In) R Software
nlme <- groupedData(height ~ age | id, data = as.data.frame(nlme),labels = list(x = "Print size", y = "Reading speed"), units = list(x = "(logMAR)", y = "(logWPM)"))
nlme <- nlme(height ~ SSasymp(age, Asym, R0, lrc), data = nlme, fixed = Asym + R0 + lrc ~ 1, random = Asym ~ 1, start = c(Asym = 103, R0 = -8.5, lrc = -3.3))
summary(nlme)
# Nonlinear mixed-effects model fit by maximum likelihood Use nlme With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished
