## Code for Venn Diagram (Created in R Studio):


    install.packages('VennDiagram')
    library(VennDiagram)
    draw.pairwise.venn(area1 = 901,
                       area2 = 2694,
                       cross.area = 673,
                       #category = c("HTAS-1 Bound Genes: 901","HTZ-1 Bound"),
                       fill = c("#B2BABB","#5499C7"),
                       ext.text = TRUE,
                       ext.percent = c(0.1,0.1,0.1),
                       label.col = rep("gray10",3),
                       lwd = 0,
                       cex = 2,
                       fontface = rep("bold",3),
                       fontfamily = rep("sans",3), 
                       cat.cex = 1.5,
                       cat.fontface = rep("plain",2),
                       cat.fontfamily = rep("sans",2),
                       cat.pos = c(0, 0)
                       #print.mode = c("percent","raw")
    )

## Code for Hypergeomtric test (used in R Studio – don’t mind variable names LOL):
      #significance in overlap
      overlap <- 673
      htas.up <- 2694
      genome <- 19826 
      gene <- 901

      phyper(overlap-1,htas.up,genome-htas.up,gene, lower.tail= FALSE)
      
