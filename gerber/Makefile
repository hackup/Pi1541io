PROJECT=Pi1541io
all: $(PROJECT).zip

rename_old:
	$(shell [[ -f $(PROJECT)-B.Cu.gbl ]] && mv $(PROJECT)-B.Cu.gbl $(PROJECT).gbl)
	$(shell [[ -f $(PROJECT)-B.Mask.gbs ]] && mv $(PROJECT)-B.Mask.gbs $(PROJECT).gbs)
	$(shell [[ -f $(PROJECT)-B.SilkS.gbo ]] && mv $(PROJECT)-B.SilkS.gbo $(PROJECT).gbo)
	$(shell [[ -f $(PROJECT)-F.Cu.gtl ]] && mv $(PROJECT)-F.Cu.gtl $(PROJECT).gtl)
	$(shell [[ -f $(PROJECT)-F.Mask.gts ]] && mv $(PROJECT)-F.Mask.gts $(PROJECT).gts)
	$(shell [[ -f $(PROJECT)-F.SilkS.gto ]] && mv $(PROJECT)-F.SilkS.gto $(PROJECT).gto)
	$(shell [[ -f $(PROJECT)-Edge.Cuts.gm1 ]] && mv $(PROJECT)-Edge.Cuts.gm1 $(PROJECT).gko)
	$(shell chmod -x $(PROJECT)*)

rename:
	$(shell [[ -f $(PROJECT)-Edge.Cuts.gm1 ]] && mv $(PROJECT)-Edge.Cuts.gm1 $(PROJECT).gko)

$(PROJECT).zip: rename
	zip $(PROJECT).zip $(PROJECT)*.gt? $(PROJECT)*.gb? $(PROJECT)*.drl $(PROJECT)*.gko

clean:
	rm -f $(PROJECT).zip
