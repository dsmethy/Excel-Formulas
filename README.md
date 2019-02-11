# Excel-Formulas
This is  a repo of simple and complicated formulas to use in spreadsheets like Excel 

=VLOOKUP(D5,'Lookup Reference Sheet'!$C:$E,3,FALSE)

=IF(C5="Facebook",VLOOKUP(D5,'FB-IG Ads Manager'!$C:$U,19,FALSE),IF('Totals Sheet'!C5="Instagram",VLOOKUP(D5,'FB-IG Ads Manager'!$C:$U,19,FALSE),IF('Totals Sheet'!C5="LinkedIn",VLOOKUP('Totals Sheet'!D5,'LinkedIn Ads Manager'!$M:$CC,2,FALSE),IF('Totals Sheet'!C5="Twitter",VLOOKUP(D5,'Twitter Ads Manager'!$C:$D,2,FALSE),"-"))))

[To find the Platform]
=VLOOKUP(D5,'Lookup Reference Sheet'!$C:$E,3,FALSE)

[To find the Objective]
=IF(C5="Facebook",VLOOKUP(D5,'FB-IG Ads Manager'!$C:$U,19,FALSE),IF('Totals Sheet'!C5="Instagram",VLOOKUP(D5,'FB-IG Ads Manager'!$C:$U,19,FALSE),IF('Totals Sheet'!C5="LinkedIn",VLOOKUP('Totals Sheet'!D5,'LinkedIn Ads Manager'!$M:$CC,2,FALSE),IF('Totals Sheet'!C5="Twitter",VLOOKUP(D5,'Twitter Ads Manager'!$C:$D,2,FALSE),"-"))))

[Dates]
VLOOKUP for Start and End
Start: =IF(C5="Facebook",VLOOKUP(D5,'FB-IG Ads Manager'!$C:$Y,20,FALSE),IF('Totals Sheet'!C5="Instagram",VLOOKUP(D5,'FB-IG Ads Manager'!$C:$Y,20,FALSE),IF('Totals Sheet'!C5="LinkedIn",VLOOKUP('Totals Sheet'!D5,'LinkedIn Ads Manager'!$M:$CC,2,FALSE),IF('Totals Sheet'!C5="Twitter",VLOOKUP(D5,'Twitter Ads Manager'!$C:$W,9,FALSE),"-"))))
***Look into LinkedIn***
End: =IF(C5="Facebook",VLOOKUP(D5,'FB-IG Ads Manager'!$C:$Y,12,FALSE),IF('Totals Sheet'!C5="Instagram",VLOOKUP(D5,'FB-IG Ads Manager'!$C:$Y,12,FALSE),IF('Totals Sheet'!C5="LinkedIn",VLOOKUP('Totals Sheet'!D5,'LinkedIn Ads Manager'!$M:$CC,2,FALSE),IF('Totals Sheet'!C5="Twitter",VLOOKUP(D5,'Twitter Ads Manager'!$C:$W,10,FALSE),"-"))))

[Pulling sessions from the GA sheets]
=IF(C5="Facebook",VLOOKUP(D5,’GA Facebook’!$A:$U,19,FALSE),IF('Totals Sheet'!C5="Instagram",VLOOKUP(D5,’GA Instagram’!$A:$U,19,FALSE),IF('Totals Sheet'!C5="LinkedIn",VLOOKUP('Totals Sheet'!D5,’GA LinkedIn’!$A:$CC,2,FALSE),IF('Totals Sheet'!C5="Twitter",VLOOKUP(D5,’GA Twitter’!$A:$D,2,FALSE),"-"))))

[Getting the dates from platforms]
! <> =CONCATENATE((D5,'FB-IG Ads Manager'!$C:$X,20,FALSE),VLOOKUP(D5,'FB-IG Ads Manager'!$C:$X,12,FALSE))
=VLOOKUP(D5,'FB-IG Ads Manager'!$C:$X,20,FALSE)&" "&VLOOKUP(D5,'FB-IG Ads Manager'!$C:$X,12,FALSE)

[Start Date]
=IF(C5="Facebook",VLOOKUP(D5,'FB-IG Ads Manager'!$C:$V,20,FALSE),IF(C5="Instagram",VLOOKUP(D5,'FB-IG Ads Manager'!$C:$Y,20,FALSE),IF(C5="LinkedIn",VLOOKUP(D5,'LinkedIn Ads Manager'!$K:$M,2,FALSE),IF(C5="Twitter",VLOOKUP(D5,'Twitter Ads Manager'!$C:$W,10,FALSE),"-"))))

[End Date]
=IF(C5="Facebook",VLOOKUP(D5,'FB-IG Ads Manager'!$C:$V,12,FALSE),IF(C5="Instagram",VLOOKUP(D5,'FB-IG Ads Manager'!$C:$Y,12,FALSE),IF(C5="LinkedIn",VLOOKUP(D5,'LinkedIn Ads Manager'!$K:$M,3,FALSE),IF(C5="Twitter",VLOOKUP(D5,'Twitter Ads Manager'!$C:$W,10,FALSE),"-"))))

[Program Name]
=VLOOKUP(D5,'Lookup Reference Sheet'!$C:$F,4,FALSE)

[Lead Form]
=IF(C5="Facebook",VLOOKUP(D5,'FB1'!$C:$CC,19,FALSE),IF('Totals Sheet'!C5="Instagram",VLOOKUP(D5,'FB1'!$C:$CC,19,FALSE),IF('Totals Sheet'!C5="LinkedIn",VLOOKUP('Totals Sheet'!D5,'LinkedIn Ads Manager'!$K:$CA,52,FALSE),"-")))

[Sessions]
=IF('Totals Sheet'!C7='Facebook',VLOOKUP('Totals Sheet'!E7,'GA Facebook'!$D:$M,2,FALSE),IF('Totals Sheet'!C7='Instagram',VLOOKUP('Totals Sheet'!E7,'GA Instagram'!$D:$M,2,FALSE),IF('Totals Sheet'!C7='LinkedIn',VLOOKUP('Totals Sheet'!E7,'GA LinkedIn'!$D:$M,2,FALSE),IF('Totals Sheet'!C7='Twitter',VLOOKUP('Totals Sheet'!E7,'GA Twitter'!$D:$M,2,FALSE),"-"))))
