# SPDX-License-Identifier: GPL-2.0
ccflags-y := -I$(srctree)/include/drm -I$(srctree)/techpack/display/msm -I$(srctree)/techpack/display/msm/dsi -I$(srctree)/techpack/display/msm/dp
ccflags-y += -I$(srctree)/techpack/display/msm/sde
ccflags-y += -I$(srctree)/techpack/display/rotator

ifeq ($(CONFIG_DISPLAY_SAMSUNG),y)
ccflags-y += -I$(srctree)/include/drm
ccflags-y += -I$(srctree)/techpack/display/msm
ccflags-y += -I$(srctree)/techpack/display/msm/dsi
ccflags-y += -I$(srctree)/techpack/display/msm/sde
ccflags-y += -I$(srctree)/drivers/clk/qcom/
ccflags-y += -I$(srctree)/techpack/display/msm/samsung
endif

msm_drm-$(CONFIG_DRM_MSM_DP) += dp/dp_usbpd.o \
	dp/dp_parser.o \
	dp/dp_power.o \
	dp/dp_catalog.o \
	dp/dp_catalog_v420.o \
	dp/dp_catalog_v200.o \
	dp/dp_aux.o \
	dp/dp_panel.o \
	dp/dp_link.o \
	dp/dp_ctrl.o \
	dp/dp_audio.o \
	dp/dp_debug.o \
	dp/dp_hpd.o \
	dp/dp_gpio_hpd.o \
	dp/dp_lphw_hpd.o \
	dp/dp_display.o \
	dp/dp_drm.o \
	dp/dp_hdcp2p2.o \
	dp/dp_mst_drm.o \

# sec displayport
msm_drm-$(CONFIG_SEC_DISPLAYPORT) += dp/secdp_sysfs.o \
	dp/secdp_logger.o \
	dp/secdp_unit_test.o \

msm_drm-$(CONFIG_SEC_DISPLAYPORT_BIGDATA) += dp/displayport_bigdata.o \

msm_drm-$(CONFIG_DRM_MSM_SDE) += sde/sde_crtc.o \
	sde/sde_encoder.o \
	sde/sde_encoder_phys_vid.o \
	sde/sde_encoder_phys_cmd.o \
	sde/sde_irq.o \
	sde/sde_core_irq.o \
	sde/sde_core_perf.o \
	sde/sde_rm.o \
	sde/sde_kms_utils.o \
	sde/sde_kms.o \
	sde/sde_plane.o \
	sde/sde_connector.o \
	sde/sde_color_processing.o \
	sde/sde_vbif.o \
	sde_io_util.o \
	sde/sde_hw_reg_dma_v1_color_proc.o \
	sde/sde_hw_color_proc_v4.o \
	sde/sde_hw_ad4.o \
	sde/sde_hw_uidle.o \
	sde_edid_parser.o \
	sde_hdcp_1x.o \
	sde_hdcp_2x.o \
	sde/sde_hw_catalog.o \
	sde/sde_hw_cdm.o \
	sde/sde_hw_dspp.o \
	sde/sde_hw_intf.o \
	sde/sde_hw_lm.o \
	sde/sde_hw_ctl.o \
	sde/sde_hw_util.o \
	sde/sde_hw_sspp.o \
	sde/sde_hw_wb.o \
	sde/sde_hw_pingpong.o \
	sde/sde_hw_top.o \
	sde/sde_hw_interrupts.o \
	sde/sde_hw_vbif.o \
	sde/sde_hw_blk.o \
	sde/sde_formats.o \
	sde_power_handle.o \
	sde/sde_hw_color_processing_v1_7.o \
	sde/sde_reg_dma.o \
	sde/sde_hw_reg_dma_v1.o \
	sde/sde_hw_dsc.o \
	sde/sde_hw_ds.o \
	sde/sde_fence.o \
	sde/sde_hw_qdss.o \
	sde_dbg.o \
	sde_dbg_evtlog.o \

msm_drm-$(CONFIG_DRM_SDE_WB) += sde/sde_wb.o \
	sde/sde_encoder_phys_wb.o \

msm_drm-$(CONFIG_DRM_SDE_RSC) += sde_rsc.o \
	sde_rsc_hw.o \
	sde_rsc_hw_v3.o \

msm_drm-$(CONFIG_DRM_MSM_DSI) += dsi/dsi_phy.o \
	dsi/dsi_pwr.o \
	dsi/dsi_phy.o \
	dsi/dsi_phy_hw_v2_0.o \
	dsi/dsi_phy_hw_v3_0.o \
	dsi/dsi_phy_hw_v4_0.o \
	dsi/dsi_phy_timing_calc.o \
	dsi/dsi_phy_timing_v2_0.o \
	dsi/dsi_phy_timing_v3_0.o \
	dsi/dsi_phy_timing_v4_0.o \
	dsi/dsi_ctrl_hw_cmn.o \
	dsi/dsi_ctrl_hw_1_4.o \
	dsi/dsi_ctrl_hw_2_0.o \
	dsi/dsi_ctrl_hw_2_2.o \
	dsi/dsi_ctrl.o \
	dsi/dsi_catalog.o \
	dsi/dsi_drm.o \
	dsi/dsi_display.o \
	dsi/dsi_panel.o \
	dsi/dsi_clk_manager.o \
	dsi/dsi_display_test.o \

msm_drm-$(CONFIG_DSI_PARSER) += dsi/dsi_parser.o \

msm_drm-$(CONFIG_DRM_MSM) += \
	msm_atomic.o \
	msm_fb.o \
	msm_iommu.o \
	msm_drv.o \
	msm_gem.o \
	msm_gem_prime.o \
	msm_gem_vma.o \
	msm_smmu.o \
	msm_prop.o \
	msm_notifier.o\

obj-$(CONFIG_DRM_MSM)	+= msm_drm.o

obj-$(CONFIG_DRM_FBDEV_EMULATION) += msm_fbdev.o


msm_drm-$(CONFIG_DISPLAY_SAMSUNG) += samsung/PBA_BOOTING/ss_dsi_panel_PBA_BOOTING_fhd.o

msm_drm-$(CONFIG_PANEL_S6E8FC1_AMS660XR01_HD) += samsung/S6E8FC1_AMS660XR01/ss_dsi_panel_S6E8FC1_AMS660XR01.o

msm_drm-$(CONFIG_DISPLAY_SAMSUNG) += samsung/ss_dsi_panel_sysfs.o \
	samsung/ss_dsi_panel_debug.o \
	samsung/ss_dsi_panel_common.o \
	samsung/ss_dsi_mdnie_lite_common.o \
	samsung/ss_dsi_smart_dimming_common.o \
	samsung/ss_interpolation_common.o \
	samsung/ss_flash_table_data_common.o \
	samsung/ss_dpui_common.o \
	samsung/ss_ddi_poc_common.o \
	samsung/ss_ddi_spi_common.o \
	samsung/ss_copr_common.o

msm_drm-$(CONFIG_DISPLAY_SAMSUNG) += samsung/SELF_DISPLAY/self_display_6W3.o \
	samsung/SELF_DISPLAY/self_display_FA7.o \
	samsung/SELF_DISPLAY/self_display_FA9.o \
	samsung/SELF_DISPLAY/self_display_FAB.o \
	samsung/SELF_DISPLAY/self_display_HA8.o \
	samsung/SELF_DISPLAY/self_display_HA9.o \
	samsung/SELF_DISPLAY/self_display_HAB.o \
	samsung/SELF_DISPLAY/self_display_HAC.o \
	samsung/SELF_DISPLAY/self_display_HAD.o \
	samsung/SELF_DISPLAY/self_display_UM1.o \
	samsung/SELF_DISPLAY/self_display_XA0.o \
	samsung/SELF_DISPLAY/self_display_XA1.o \
	samsung/SELF_DISPLAY/self_display_FC1.o \
	samsung/SELF_DISPLAY/self_display_SW83109.o \
	samsung/SELF_DISPLAY/self_display_HAB_AMB667AN01.o \
	samsung/SELF_DISPLAY/self_display_FC3.o


msm_drm-$(CONFIG_DISPLAY_SAMSUNG) += samsung/MAFPC/ss_dsi_mafpc_FAB.o \
	samsung/MAFPC/ss_dsi_mafpc_HAB.o \
	samsung/MAFPC/ss_dsi_mafpc_HAC.o \
	samsung/MAFPC/ss_dsi_mafpc_HAD.o \
	samsung/MAFPC/ss_dsi_mafpc_XA1.o