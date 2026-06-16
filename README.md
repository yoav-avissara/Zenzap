[zenzap-v9-interactive.html](https://github.com/user-attachments/files/28987538/zenzap-v9-interactive.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Zenzap — Teams & Locations (Interactive Walkthrough)</title>
<style>
*{box-sizing:border-box;margin:0;padding:0}
body{background:#111;font-family:-apple-system,'SF Pro Text','Helvetica Neue',sans-serif;display:flex;flex-direction:column;align-items:center;padding:90px 24px 48px;gap:14px}
.ph{text-align:center;color:#fff;max-width:600px}
.ph h1{font-size:24px;font-weight:700;letter-spacing:-.3px;margin-bottom:8px}
.ph p{font-size:14px;color:#666;line-height:1.55}
.ph .vb{display:inline-block;background:#4A6CF7;color:#fff;font-size:11px;font-weight:700;padding:3px 10px;border-radius:6px;margin-bottom:12px;letter-spacing:.5px}

.sg{display:flex;flex-direction:column;align-items:center;gap:14px;width:100%}
.sg-n{font-size:10px;font-weight:700;letter-spacing:1.2px;text-transform:uppercase;color:#444;align-self:flex-start;max-width:860px;width:100%}
.sg-t{font-size:15px;font-weight:700;color:#ccc;align-self:flex-start;margin-top:-4px;max-width:860px;width:100%}

.variant-row{display:flex;gap:20px;justify-content:center;flex-wrap:wrap}
.variant-wrap{display:flex;flex-direction:column;align-items:center;gap:8px}
.variant-lbl{font-size:10px;font-weight:700;letter-spacing:.7px;text-transform:uppercase;color:#555;text-align:center;max-width:320px}
.variant-lbl.blue{color:#4A6CF7}.variant-lbl.amber{color:#F5A623}

.phone{width:320px;background:#fff;border-radius:44px;overflow:hidden;box-shadow:0 32px 80px rgba(0,0,0,.75),0 0 0 1px rgba(255,255,255,.06)}
.phone.full{width:393px;border-radius:50px}

.sb{background:#fff;padding:14px 24px 6px;display:flex;justify-content:space-between;align-items:center}
.sb-t{font-size:14px;font-weight:600;color:#000}
.sb-r{font-size:11px;color:#000}

.hh{background:#fff;padding:9px 14px;display:flex;align-items:center;gap:7px;border-bottom:.5px solid #F0F0F0}
.hh-ic{width:32px;height:32px;background:#F5F5F5;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:14px;color:#888}
.hh-pill{flex:1;background:#F5F5F5;border-radius:18px;padding:7px 12px;display:flex;align-items:center;justify-content:flex-end;gap:7px}
.hh-name{font-size:13px;font-weight:600;color:#000}
.hh-av{width:24px;height:24px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:9px;font-weight:700;color:#fff}

.ftabs{display:flex;gap:6px;padding:8px 14px;background:#fff;border-bottom:.5px solid #F0F0F0;overflow-x:auto}
.ftabs::-webkit-scrollbar{display:none}
.fp{padding:6px 12px;border-radius:16px;font-size:12px;font-weight:500;white-space:nowrap;border:1px solid #DCDCDC;background:#fff;color:#333;cursor:pointer}
.fp.on{background:#4A6CF7;color:#fff;border-color:#4A6CF7}

.nb{background:#fff;padding:11px 18px;display:flex;align-items:center;justify-content:space-between;border-bottom:.5px solid #EBEBEB}
.nb-back{width:30px;height:30px;background:#F0F0F0;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:14px;color:#666;cursor:pointer}
.nb-title{font-size:16px;font-weight:600;color:#000}
.nb-sp{width:30px}

.sec{background:#F0F0F0;padding:5px 18px;font-size:11px;color:#888;width:100%;letter-spacing:.2px}
.srow{background:#fff;padding:12px 18px;display:flex;align-items:center;justify-content:space-between;border-bottom:.5px solid #EBEBEB}
.srow:last-child{border-bottom:none}
.srow-l{font-size:15px;color:#000}
.srow-l2{font-size:12px;color:#888;margin-top:2px}
.srow-r{font-size:13px;color:#AAA;display:flex;align-items:center;gap:3px}
.chev{color:#D0D0D0;font-size:12px}

.tog{width:46px;height:28px;border-radius:14px;position:relative;flex-shrink:0;cursor:pointer}
.tog.on{background:#34C759}.tog.off{background:#E5E5EA}
.tog::after{content:'';width:24px;height:24px;background:#fff;border-radius:50%;position:absolute;top:2px;box-shadow:0 2px 4px rgba(0,0,0,.2);transition:left .15s}
.tog.on::after{left:20px}.tog.off::after{left:2px}

.tabbar{background:#fff;border-top:.5px solid #EBEBEB;padding:9px 0 20px;display:flex;justify-content:space-around}
.tab{display:flex;flex-direction:column;align-items:center;gap:3px;flex:1}
.tab-iw{width:32px;height:32px;display:flex;align-items:center;justify-content:center;border-radius:9px}
.tab.active .tab-iw{background:#EEF1FE}
.tab svg{width:20px;height:20px;color:#C8C8C8}
.tab.active svg{color:#4A6CF7}
.hh-ic svg,.nb-back svg{width:17px;height:17px}
.hh-ic svg{color:#888}
.nb-back svg{color:#666}
.fab svg{width:15px;height:15px;color:#fff}
.tab-l{font-size:9px;color:#C8C8C8;font-weight:500}
.tab.active .tab-l{color:#4A6CF7}

.crow{background:#fff;padding:11px 14px 11px 18px;display:flex;align-items:center;gap:10px;border-bottom:.5px solid #F2F2F2}
.cav-r{width:40px;height:40px;border-radius:10px;display:flex;align-items:center;justify-content:center;font-size:18px;flex-shrink:0}
.cav-c{width:40px;height:40px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:12px;font-weight:700;color:#fff;flex-shrink:0}
.ci{flex:1;min-width:0}
.cn{font-size:14px;font-weight:600;color:#000}
.cp{font-size:12px;color:#AAA;white-space:nowrap;overflow:hidden;text-overflow:ellipsis;margin-top:1px}
.cm{display:flex;flex-direction:column;align-items:flex-end;gap:3px;flex-shrink:0}
.ct{font-size:11px;color:#AAA}
.cbadge{background:#4A6CF7;color:#fff;font-size:10px;font-weight:700;padding:2px 6px;border-radius:8px}

.nudge{margin:10px 14px 0;border-radius:15px;padding:14px;position:relative}
.nudge.blue{background:linear-gradient(135deg,#EEF1FE,#E4EBFF);border:1px solid rgba(74,108,247,.12)}
.nudge.amber{background:linear-gradient(135deg,#FFF8E7,#FFF1CC);border:1px solid rgba(245,166,35,.2)}
.nudge-x{position:absolute;top:10px;right:10px;width:19px;height:19px;background:rgba(0,0,0,.07);border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:9px;color:#666}
.nudge-icon{font-size:20px;margin-bottom:6px;display:block}
.nudge-title{font-size:13px;font-weight:700;color:#111;margin-bottom:3px}
.nudge-body{font-size:12px;color:#555;line-height:1.45;margin-bottom:10px}
.nudge-prog{display:flex;align-items:center;gap:6px;margin-bottom:8px}
.nudge-prog-bar{flex:1;height:3px;background:rgba(245,166,35,.15);border-radius:2px;overflow:hidden}
.nudge-prog-fill{height:100%;border-radius:2px}
.nudge-prog-lbl{font-size:10px;font-weight:600;white-space:nowrap}
.nudge-btn{display:inline-block;padding:8px 16px;border-radius:10px;font-size:12px;font-weight:700;color:#fff;cursor:pointer}
.nudge-btn.blue{background:#4A6CF7}
.nudge-btn.amber{background:#F5A623}

/* wizard progress */
.wprog{background:#fff;padding:11px 18px 9px;display:flex;gap:5px;border-bottom:.5px solid #EBEBEB}
.ws{height:4px;border-radius:2px;flex:1}
.ws.done{background:#4A6CF7}
.ws.now{background:#4A6CF7;opacity:.3}
.ws.next{background:#EBEBEB}

.wb{padding:16px 18px 12px;background:#fff}
.wstep{font-size:11px;font-weight:700;color:#4A6CF7;text-transform:uppercase;letter-spacing:.5px;margin-bottom:3px}
.wtitle{font-size:20px;font-weight:700;color:#000;margin-bottom:4px;line-height:1.2}
.wsub{font-size:13px;color:#777;line-height:1.4;margin-bottom:14px}

/* locations step */
.loc-input-row{background:#fff;padding:11px 18px;display:flex;align-items:center;gap:10px;border-bottom:.5px solid #F2F2F2}
.loc-dot{width:8px;height:8px;border-radius:50%;background:#4A6CF7;flex-shrink:0}
.loc-input{flex:1;font-size:15px;font-weight:500;color:#000;border:none;outline:none;background:transparent;font-family:inherit}
.loc-del{font-size:16px;color:#D8D8D8;flex-shrink:0;cursor:pointer}
.loc-add-row{padding:11px 18px;display:flex;align-items:center;gap:10px;background:#fff;cursor:pointer}
.loc-add-txt{font-size:14px;color:#4A6CF7;font-weight:600}

/* industry grid */
.igrid{display:grid;grid-template-columns:1fr 1fr;gap:8px;margin-bottom:12px}
.icard{background:#F7F7F7;border-radius:12px;padding:12px 10px;display:flex;flex-direction:column;align-items:center;gap:5px;border:2px solid transparent;text-align:center;cursor:pointer}
.icard.sel{border-color:#4A6CF7;background:#EEF1FE}
.icard-icon{font-size:20px}
.icard-lbl{font-size:12px;font-weight:600;color:#111}

/* AI card */
.aicard{background:#F7F7F7;border-radius:12px;padding:12px;margin-bottom:5px}
.aihdr{display:flex;align-items:flex-start;gap:6px;margin-bottom:8px}
.aibadge{background:linear-gradient(135deg,#667EEA,#764BA2);color:#fff;font-size:9px;font-weight:700;padding:2px 6px;border-radius:4px;flex-shrink:0;margin-top:1px}
.ait{font-size:13px;font-weight:600;color:#000}
.chips{display:flex;flex-wrap:wrap;gap:6px;align-items:center}
.chip{display:flex;align-items:center;gap:3px;background:#fff;border-radius:16px;padding:5px 10px;font-size:12px;font-weight:500;color:#111;border:1px solid #EBEBEB}
.chip-scope{font-size:10px;color:#C8C8C8;font-weight:400}
.chip-x{color:#CCC;font-size:12px;margin-left:1px}
.chip-add{background:#EEF1FE;border:1.5px dashed #4A6CF7;color:#4A6CF7;font-size:12px;font-weight:600;border-radius:16px;padding:5px 10px}
.chip-empty{font-size:12px;color:#BBB;padding:5px 0}

/* tier editor */
.tier-editor{background:#F7F7F7;border-radius:12px;padding:12px;margin:0 18px 14px}
.tier-hdr{display:flex;align-items:flex-start;gap:6px;margin-bottom:10px}
.tier-badge{background:linear-gradient(135deg,#1F4E79,#2E75B6);color:#fff;font-size:9px;font-weight:700;padding:2px 6px;border-radius:4px;flex-shrink:0;margin-top:1px}
.tier-title{font-size:13px;font-weight:600;color:#000}
.tier-rows{display:flex;flex-direction:column;gap:7px}
.tier-row{display:flex;align-items:flex-start;gap:6px;border-radius:8px;transition:background .12s}
.tier-row.drag-over{background:#EEF1FE}
.tier-handle{color:#D8D8D8;font-size:13px;flex-shrink:0;width:13px;text-align:center;padding-top:9px}
.tier-row[draggable="true"]{cursor:grab}
.tier-row[draggable="true"]:active{cursor:grabbing}
.tier-num{width:20px;height:20px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:9px;font-weight:700;color:#fff;flex-shrink:0;margin-top:7px}
.tier-pill-wrap{flex:1;display:flex;flex-direction:column;gap:3px;min-width:0}
.tier-pill{background:#fff;border-radius:9px;padding:7px 10px;display:flex;align-items:center;justify-content:space-between;border:1.5px solid #EBEBEB}
.tier-pill.locked{border-color:#C8D8EA;background:#F0F5FA}
.tier-pill.editing{border-color:#4A6CF7;background:#F8F9FF}
.tier-name{font-size:13px;font-weight:600;color:#000}
.tier-name.locked{color:#2E75B6;font-size:12px}
.tier-actions{display:flex;align-items:center;gap:5px;flex-shrink:0}
.tier-edit{font-size:11px;color:#4A6CF7;font-weight:600;cursor:pointer}
.tier-del{font-size:13px;color:#D8D8D8;cursor:pointer}
.tier-del.off{color:#F0F0F0;cursor:default}
.tier-hint{font-size:11px;color:#AAA;padding:0 2px;line-height:1.35}
.tier-hint.locked{color:#7AA8C8}
.tier-hint.updated{background:#EEF1FE;border-radius:5px;padding:2px 6px;color:#5C6F99}
.tier-add{border:1.5px dashed #4A6CF7;background:#EEF1FE;border-radius:9px;padding:8px 10px;text-align:center;font-size:12px;font-weight:600;color:#4A6CF7;margin-top:6px;cursor:pointer}

/* Step 3 — progressive disclosure */
.tier-summary{display:flex;flex-direction:column;gap:6px;margin-bottom:10px}
.tier-sum-row{background:#fff;border-radius:9px;padding:8px 10px;display:flex;align-items:center;gap:8px;border:1.5px solid #EBEBEB}
.tier-sum-num{width:20px;height:20px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:9px;font-weight:700;color:#fff;flex-shrink:0}
.tier-sum-info{flex:1}
.tier-sum-name{font-size:13px;font-weight:600;color:#000}
.tier-sum-hint{font-size:11px;color:#AAA;margin-top:1px}
.cust-toggle{display:flex;align-items:center;justify-content:center;gap:5px;font-size:12px;font-weight:700;color:#4A6CF7;padding:8px 0 4px;cursor:pointer;user-select:none}
.cust-editor{display:none}
.cust-editor.open{display:block}

/* Step 4 — bulk-actions collapse */
.bulk-toggle{display:flex;align-items:center;gap:6px;font-size:12px;font-weight:700;color:#4A6CF7;padding:8px 14px;cursor:pointer;user-select:none;background:#fff;border-top:.5px solid #F2F2F2}
.bulk-section{display:none}
.bulk-section.open{display:block}

/* communication boundaries (Screen 4) */
.div-lbl{padding:9px 18px 7px;display:flex;align-items:center;gap:9px;background:#fff}
.div-line{flex:1;height:.5px;background:#EBEBEB}
.div-txt{font-size:10px;font-weight:700;color:#C8C8C8;text-transform:uppercase;letter-spacing:.6px;flex-shrink:0}
.bound-card{background:#F7F7F7;border-radius:12px;padding:12px;margin:0 18px 10px}
.bound-hdr{display:flex;align-items:flex-start;justify-content:space-between;gap:10px}
.bound-title{font-size:13px;font-weight:700;color:#000}
.bound-sub{font-size:11px;color:#999;margin-top:2px}
.bound-list{display:flex;flex-direction:column;gap:5px;margin-top:9px;padding-top:9px;border-top:1px solid #ECECEC}
.bound-item{font-size:11px;color:#5C8A5C;line-height:1.4;display:flex;gap:6px}
.bound-item.neg{color:#B0413E}
.bound-exception{margin-top:9px;padding-top:9px;border-top:1px solid #ECECEC}
.bound-exception-lbl{font-size:11px;font-weight:700;color:#888;margin-bottom:6px}
.bound-radio{font-size:12px;color:#444;padding:6px 0;display:flex;align-items:center;gap:8px;cursor:pointer}
.bound-radio-dot{width:16px;height:16px;border-radius:50%;border:2px solid #D8D8D8;flex-shrink:0;display:flex;align-items:center;justify-content:center}
.bound-radio.sel .bound-radio-dot{border-color:#4A6CF7}
.bound-radio.sel .bound-radio-dot::after{content:'';width:8px;height:8px;border-radius:50%;background:#4A6CF7}
.bound-radio.sel{color:#1F4E79;font-weight:600}

/* contacts screen */
.crow-dim{opacity:.55;cursor:pointer}
.redirect-note{display:none;font-size:11px;color:#4A6CF7;background:#EEF1FE;border-radius:8px;padding:7px 10px;margin:0 14px 8px 64px}
.redirect-note.show{display:block}

/* assign */
.brow{background:#fff;padding:10px 14px;display:flex;align-items:center;gap:8px;border-bottom:.5px solid #F2F2F2}
.bav{width:32px;height:32px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:11px;font-weight:700;color:#fff;flex-shrink:0}
.bname{font-size:13px;font-weight:600;color:#000;flex:1;min-width:0;white-space:nowrap;overflow:hidden;text-overflow:ellipsis}
.bdds{display:flex;gap:4px;flex-shrink:0;align-items:center}
.bdd{background:#EEF1FE;border-radius:6px;padding:4px 7px;font-size:11px;font-weight:600;color:#4A6CF7;white-space:nowrap}
.bdd.un{color:#C8C8C8;background:#fff;border:1px dashed #D8D8D8}
.bdd.gr{background:#E8F5E9;color:#2E7D32}
.bdd.updated{background:#fff;border:1.5px solid #4A6CF7;color:#1F4E79}

.bchk{width:20px;height:20px;border-radius:6px;border:1.5px solid #D8D8D8;flex-shrink:0;display:flex;align-items:center;justify-content:center;font-size:12px;font-weight:700;color:#fff;cursor:pointer}
.bchk.on{background:#4A6CF7;border-color:#4A6CF7}

.bulk-bar{background:#EEF1FE;border:1px solid rgba(74,108,247,.18);border-radius:12px;padding:10px 12px;margin:10px 14px 0;flex-direction:column;gap:7px}
.bulk-top{display:flex;align-items:center;justify-content:space-between}
.bulk-count{font-size:12px;font-weight:700;color:#1F4E79}
.bulk-clear{font-size:11px;font-weight:600;color:#9AA5C9;cursor:pointer}
.bulk-row{display:flex;align-items:center;gap:6px}
.bulk-apply{font-size:12px;font-weight:700;color:#fff;background:#4A6CF7;padding:7px 14px;border-radius:8px;white-space:nowrap;margin-left:auto;cursor:pointer}
.bulk-note{font-size:11px;color:#8893B5;line-height:1.4}

/* dropdown pills (Screen 5) */
.bdd-select{appearance:none;-webkit-appearance:none;-moz-appearance:none;background-color:#EEF1FE;border:none;border-radius:6px;padding:4px 18px 4px 7px;font-size:11px;font-weight:600;color:#4A6CF7;font-family:inherit;cursor:pointer;background-image:url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="8" height="8" viewBox="0 0 8 8"><path fill="%234A6CF7" d="M0 2l4 4 4-4z"/></svg>');background-repeat:no-repeat;background-position:right 6px center}
.bdd-select.gr{background-color:#E8F5E9;color:#2E7D32;background-image:url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="8" height="8" viewBox="0 0 8 8"><path fill="%232E7D32" d="M0 2l4 4 4-4z"/></svg>')}
.bdd-select.un{background-color:#fff;border:1px dashed #D8D8D8;color:#C8C8C8;background-image:url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="8" height="8" viewBox="0 0 8 8"><path fill="%23C8C8C8" d="M0 2l4 4 4-4z"/></svg>')}
.bdd-select.updated{background-color:#fff;border:1.5px solid #4A6CF7;color:#1F4E79;background-image:url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="8" height="8" viewBox="0 0 8 8"><path fill="%234A6CF7" d="M0 2l4 4 4-4z"/></svg>')}
.bulk-pill-select{appearance:none;-webkit-appearance:none;-moz-appearance:none;background-color:#fff;border:1.5px solid #4A6CF7;border-radius:8px;padding:6px 22px 6px 10px;font-size:12px;font-weight:600;color:#4A6CF7;font-family:inherit;cursor:pointer;background-image:url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="9" height="9" viewBox="0 0 8 8"><path fill="%234A6CF7" d="M0 2l4 4 4-4z"/></svg>');background-repeat:no-repeat;background-position:right 8px center}

/* delegate */
.delegate-bar{background:#EEF1FE;border-radius:10px;padding:10px 12px;display:flex;align-items:center;gap:8px;border:1px solid rgba(74,108,247,.15);margin:10px 14px 0}
.delegate-ic{font-size:16px;flex-shrink:0}
.delegate-t{flex:1}
.delegate-title{font-size:12px;font-weight:700;color:#1F4E79}
.delegate-sub{font-size:11px;color:#4A6CF7;margin-top:1px}
.delegate-btn{font-size:11px;font-weight:700;color:#fff;background:#4A6CF7;padding:5px 9px;border-radius:7px;white-space:nowrap;flex-shrink:0}

/* review */
.trow{background:#fff;padding:10px 14px;display:flex;align-items:center;gap:10px;border-bottom:.5px solid #F2F2F2}
.trow:last-child{border-bottom:none}
.ticon{width:34px;height:34px;border-radius:8px;display:flex;align-items:center;justify-content:center;font-size:16px;flex-shrink:0}
.tinfo{flex:1;min-width:0}
.tname{font-size:13px;font-weight:600;color:#000}
.tchange{font-size:11px;margin-top:2px}
.tbadge{font-size:10px;font-weight:700;padding:2px 7px;border-radius:5px;flex-shrink:0;white-space:nowrap}
.badge-r{background:#FFF0EE;color:#D32F2F}
.badge-g{background:#E8F5E9;color:#2E7D32}
.badge-gr{background:#F0F0F0;color:#888}
.badge-legacy{background:#F5F5F5;color:#999;border:1px dashed #CCCCCC}

.warnbar{margin:8px 14px 10px;background:#FFFBEE;border:1px solid rgba(245,166,35,.25);border-radius:10px;padding:10px 12px;font-size:12px;color:#7A5200;line-height:1.45}

/* member list */
.mrow{background:#fff;padding:11px 18px;display:flex;align-items:center;gap:10px;border-bottom:.5px solid #F2F2F2}
.mav{width:36px;height:36px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:12px;font-weight:700;color:#fff;flex-shrink:0}
.mi{flex:1;min-width:0}
.mn{font-size:14px;font-weight:600;color:#000}
.md{font-size:12px;color:#AAA;margin-top:1px;white-space:nowrap;overflow:hidden;text-overflow:ellipsis}
.md.warn-t{color:#D32F2F}
.mchev{color:#D8D8D8;font-size:16px}
.assign-btn{font-size:11px;font-weight:700;color:#fff;background:#4A6CF7;padding:6px 10px;border-radius:7px;white-space:nowrap;cursor:pointer;flex-shrink:0}

.ubar{margin:8px 14px;background:#FFF0EE;border:1px solid rgba(211,47,47,.12);border-radius:10px;padding:9px 12px;display:flex;align-items:center;gap:8px}
.ut{font-size:12px;color:#D32F2F;font-weight:500;flex:1}
.ubtn{font-size:12px;font-weight:700;color:#4A6CF7}

/* sort sheet overlay */
.sort-overlay{position:absolute;top:0;left:0;right:0;bottom:0;background:rgba(0,0,0,.32);display:none;flex-direction:column;justify-content:flex-end;z-index:20}
.sort-overlay.show{display:flex}
.sort-sheet{background:#F5F5F5;border-radius:18px 18px 0 0}
.sort-handle{width:34px;height:4px;background:#D0D0D0;border-radius:2px;margin:10px auto 12px}
.sort-title{font-size:15px;font-weight:600;color:#000;padding:0 16px 10px}
.sort-opts{background:#fff;margin:0 14px;border-radius:11px;overflow:hidden}
.sort-opt{padding:13px 14px;display:flex;align-items:center;justify-content:space-between;border-bottom:.5px solid #F2F2F2;font-size:14px;color:#000;cursor:pointer}
.sort-opt:last-child{border-bottom:none}
.sort-opt.sel{color:#4A6CF7;font-weight:600}
.sort-check{width:19px;height:19px;border-radius:50%;background:#4A6CF7;display:flex;align-items:center;justify-content:center;font-size:10px;color:#fff;visibility:hidden}
.sort-opt.sel .sort-check{visibility:visible}

/* employee */
.emph{background:#fff;padding:11px 18px 12px;display:flex;align-items:center;justify-content:space-between;border-bottom:.5px solid #F2F2F2}
.empw{font-size:14px;font-weight:700;color:#000}
.locbadge{background:#E8F5E9;border:1px solid rgba(46,125,50,.18);color:#2E7D32;font-size:11px;font-weight:600;padding:3px 8px;border-radius:6px}
.suprow{background:#fff;margin:10px 14px 0;border-radius:12px;padding:10px 12px;display:flex;align-items:center;gap:8px;box-shadow:0 1px 5px rgba(0,0,0,.05)}
.supav{width:34px;height:34px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:11px;font-weight:700;color:#fff;flex-shrink:0}
.supi{flex:1}
.supl{font-size:9px;font-weight:700;color:#BBB;text-transform:uppercase;letter-spacing:.3px}
.supn{font-size:13px;font-weight:600;color:#000;margin-top:1px}
.supmsg{background:#4A6CF7;color:#fff;font-size:12px;font-weight:600;padding:6px 12px;border-radius:8px;flex-shrink:0}
.seclbl{padding:11px 18px 4px;font-size:10px;font-weight:700;color:#BBB;text-transform:uppercase;letter-spacing:.4px}

.locsec{padding:10px 18px 4px;display:flex;align-items:center;justify-content:space-between}
.locname{font-size:13px;font-weight:700;color:#111;display:flex;align-items:center;gap:5px}
.loc-today{background:#34C759;color:#fff;font-size:8px;font-weight:700;padding:2px 5px;border-radius:3px}
.loc-next{background:#F0F0F0;color:#999;font-size:8px;font-weight:600;padding:2px 5px;border-radius:3px}
.loc-toggle{font-size:11px;color:#4A6CF7;font-weight:600}
.loc-coll{background:#fff;margin:0 14px 6px;border-radius:10px;padding:10px 12px;display:flex;align-items:center;justify-content:space-between}
.lc-name{font-size:13px;font-weight:500;color:#BBB}

.btn-p{background:#4A6CF7;color:#fff;font-size:15px;font-weight:600;padding:14px;border-radius:12px;text-align:center;width:100%;cursor:pointer}
.btn-s{background:#F5F5F5;color:#4A6CF7;font-size:14px;font-weight:600;padding:13px;border-radius:12px;text-align:center;width:100%;border:1.5px solid #4A6CF7;cursor:pointer}

.csv-bar{background:#F7F7F7;border-radius:10px;padding:9px 12px;display:flex;align-items:center;gap:8px;border:1px solid #EBEBEB}
.csv-t{flex:1;font-size:12px;color:#777}
.csv-btn{font-size:12px;font-weight:600;color:#4A6CF7;white-space:nowrap}

.fab{background:#4A6CF7;color:#fff;font-size:13px;font-weight:600;padding:10px 16px;border-radius:26px;display:inline-flex;align-items:center;gap:6px;box-shadow:0 3px 12px rgba(74,108,247,.32);margin:9px 14px 0}

.ann{display:flex;gap:9px;padding:12px 14px;background:rgba(255,255,255,.04);border-radius:10px;border:1px solid rgba(255,255,255,.07);width:100%;max-width:860px}
.ann-dot{width:6px;height:6px;border-radius:50%;background:#4A6CF7;flex-shrink:0;margin-top:5px}
.ann-txt{font-size:12px;color:#666;line-height:1.55}
.ann-txt strong{color:#aaa}

/* walkthrough additions */
.topnav{position:fixed;top:0;left:0;width:100%;background:#1a1a1a;border-bottom:1px solid rgba(255,255,255,.08);padding:14px 20px;display:flex;align-items:center;justify-content:space-between;z-index:100;box-sizing:border-box}
.nav-btn{background:#4A6CF7;color:#fff;border:none;padding:10px 18px;border-radius:10px;font-size:13px;font-weight:700;cursor:pointer;font-family:inherit;letter-spacing:.2px}
.nav-btn:disabled{background:#2a2a2a;color:#555;cursor:default}
.nav-indicator{color:#999;font-size:11px;font-weight:700;letter-spacing:1.5px;text-transform:uppercase}
.page{display:none}
.page.active{display:flex}
.start-btn{background:#4A6CF7;color:#fff;border:none;padding:14px 32px;border-radius:12px;font-size:15px;font-weight:700;cursor:pointer;font-family:inherit;margin-top:22px}
.hint{font-size:11px;font-weight:700;color:#4A6CF7;letter-spacing:.4px;text-align:center}

.toast{position:fixed;bottom:30px;left:50%;transform:translateX(-50%) translateY(20px);background:#1F4E79;color:#fff;padding:13px 22px;border-radius:12px;font-size:13px;font-weight:600;display:flex;align-items:center;gap:8px;box-shadow:0 8px 24px rgba(0,0,0,.35);opacity:0;transition:opacity .25s, transform .25s;z-index:300;pointer-events:none;white-space:nowrap}
.toast.show{opacity:1;transform:translateX(-50%) translateY(0)}
</style>
</head>
<body>

<svg width="0" height="0" style="position:absolute"><defs>
  <symbol id="i-admin" viewBox="0 0 24 24"><path fill="currentColor" d="M3 8l4 5 5-7 5 7 4-5v10H3z"/></symbol>
  <symbol id="i-ext" viewBox="0 0 24 24"><rect fill="currentColor" x="3" y="3" width="7" height="7" rx="1"/><rect fill="currentColor" x="14" y="3" width="7" height="7" rx="1"/><rect fill="currentColor" x="3" y="14" width="7" height="7" rx="1"/><rect fill="currentColor" x="14" y="14" width="7" height="7" rx="1"/></symbol>
  <symbol id="i-lib" viewBox="0 0 24 24"><rect fill="none" stroke="currentColor" stroke-width="2" x="3" y="3" width="18" height="18" rx="2"/><circle fill="currentColor" cx="8.5" cy="8.5" r="1.5"/><path fill="currentColor" d="M5 19l6.5-6.5 3 3L19 10v9z"/></symbol>
  <symbol id="i-contacts" viewBox="0 0 24 24"><path fill="none" stroke="currentColor" stroke-width="2.1" stroke-linecap="round" stroke-linejoin="round" d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"/><circle fill="none" stroke="currentColor" stroke-width="2.1" cx="9" cy="7" r="4"/><path fill="none" stroke="currentColor" stroke-width="2.1" stroke-linecap="round" stroke-linejoin="round" d="M23 21v-2a4 4 0 0 0-3-3.87"/><path fill="none" stroke="currentColor" stroke-width="2.1" stroke-linecap="round" stroke-linejoin="round" d="M16 3.13a4 4 0 0 1 0 7.75"/></symbol>
  <symbol id="i-home" viewBox="0 0 24 24"><path fill="none" stroke="currentColor" stroke-width="2.1" stroke-linecap="round" stroke-linejoin="round" d="M3 9l9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z"/><path fill="none" stroke="currentColor" stroke-width="2.1" stroke-linecap="round" stroke-linejoin="round" d="M9 22v-10h6v10"/></symbol>
  <symbol id="i-gear" viewBox="0 0 24 24"><circle fill="none" stroke="currentColor" stroke-width="1.8" cx="12" cy="12" r="3"/><path fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round" d="M19.4 15a1.65 1.65 0 0 0 .33 1.82l.06.06a2 2 0 0 1-2.83 2.83l-.06-.06a1.65 1.65 0 0 0-1.82-.33 1.65 1.65 0 0 0-1 1.51V21a2 2 0 0 1-4 0v-.09A1.65 1.65 0 0 0 9 19.4a1.65 1.65 0 0 0-1.82.33l-.06.06a2 2 0 0 1-2.83-2.83l.06-.06A1.65 1.65 0 0 0 4.68 15a1.65 1.65 0 0 0-1.51-1H3a2 2 0 0 1 0-4h.09A1.65 1.65 0 0 0 4.6 9a1.65 1.65 0 0 0-.33-1.82l-.06-.06a2 2 0 0 1 2.83-2.83l.06.06A1.65 1.65 0 0 0 9 4.68a1.65 1.65 0 0 0 1-1.51V3a2 2 0 0 1 4 0v.09a1.65 1.65 0 0 0 1 1.51 1.65 1.65 0 0 0 1.82-.33l.06-.06a2 2 0 0 1 2.83 2.83l-.06.06A1.65 1.65 0 0 0 19.4 9a1.65 1.65 0 0 0 1.51 1H21a2 2 0 0 1 0 4h-.09a1.65 1.65 0 0 0-1.51 1z"/></symbol>
  <symbol id="i-search" viewBox="0 0 24 24"><circle fill="none" stroke="currentColor" stroke-width="2.2" cx="11" cy="11" r="8"/><line stroke="currentColor" stroke-width="2.2" stroke-linecap="round" x1="21" y1="21" x2="16.65" y2="16.65"/></symbol>
  <symbol id="i-person-add" viewBox="0 0 24 24"><path fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" d="M16 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"/><circle fill="none" stroke="currentColor" stroke-width="2" cx="8.5" cy="7" r="4"/><line stroke="currentColor" stroke-width="2" stroke-linecap="round" x1="20" y1="8" x2="20" y2="14"/><line stroke="currentColor" stroke-width="2" stroke-linecap="round" x1="23" y1="11" x2="17" y2="11"/></symbol>
  <symbol id="i-chevl" viewBox="0 0 24 24"><polyline fill="none" stroke="currentColor" stroke-width="2.6" stroke-linecap="round" stroke-linejoin="round" points="15,18 9,12 15,6"/></symbol>
</defs></svg>

<div class="topnav">
  <button class="nav-btn" id="backBtn" onclick="prevPage()">← Back</button>
  <div class="nav-indicator" id="pageIndicator">Cover</div>
  <button class="nav-btn" id="fwdBtn" onclick="nextPage()">Forward →</button>
</div>

<div class="toast" id="toast">✓ Teams & Locations is now live</div>

<!-- PAGE 0 — Cover -->
<div class="sg page active" data-page="0">
  <div class="ph">
    <div class="vb">INTERACTIVE WALKTHROUGH</div>
    <h1>Zenzap — Teams & Locations</h1>
    <p>9 screens · trigger → 5-step wizard → management → employee chats → employee contacts<br>Toggles, location list, tier editor, dropdowns, sort, and contacts all respond to clicks — try them as you go.</p>
    <button class="start-btn" onclick="nextPage()">Start →</button>
  </div>
</div>

<!-- PAGE 1 — Screen 1: Trigger -->
<div class="sg page" data-page="1">
  <div class="sg-n">Screen 1 · 9</div>
  <div class="sg-t">Entry points — four paths, three distinct nudges</div>
  <div class="variant-row">

    <div class="variant-wrap">
      <div class="variant-lbl" style="color:#E05A1C">Free org · 20+ members · paywall first</div>
      <div class="phone">
        <div class="sb"><span class="sb-t">10:20</span><div class="sb-r">●●● 🔋</div></div>
        <div class="hh"><div class="hh-ic"><svg><use href="#i-gear"/></svg></div><div class="hh-ic"><svg><use href="#i-search"/></svg></div><div class="hh-pill"><span class="hh-name">Pizza Yoav</span><div class="hh-av" style="background:linear-gradient(135deg,#E05A1C,#B83A10)">PY</div></div></div>
        <div class="ftabs"><div class="fp on">Chats</div><div class="fp">★ Starred</div><div class="fp">Unread</div></div>
        <div style="background:#F8F8F8;padding-bottom:8px">
          <div class="nudge" style="background:linear-gradient(135deg,#FFF3EE,#FFE8DC);border:1px solid rgba(224,90,28,.15)">
            <div class="nudge-x">✕</div>
            <span class="nudge-icon">🔒</span>
            <div class="nudge-title">Upgrade to unlock Teams & Locations</div>
            <div class="nudge-body">Your workspace has 20+ members. Organize who sees what — available on Pro.</div>
            <div class="nudge-btn" style="background:#E05A1C" onclick="nextPage()">See Pro plans →</div>
          </div>
          <div class="crow"><div class="cav-r" style="background:#FFF3E0">👨‍🍳</div><div class="ci"><div class="cn">Kitchen — All Branches</div><div class="cp">Ali: New prep schedule</div></div><div class="cm"><div class="ct">Jun 3</div><div class="cbadge">4</div></div></div>
          <div class="crow"><div class="cav-r" style="background:#E3F2FD">🍷</div><div class="ci"><div class="cn">Waiters Group</div><div class="cp">Shift starts 18:00 today</div></div><div class="cm"><div class="ct">Jun 3</div></div></div>
        </div>
        <div class="tabbar">
          <div class="tab"><div class="tab-iw"><svg><use href="#i-admin"/></svg></div><div class="tab-l">Admin</div></div>
          <div class="tab"><div class="tab-iw"><svg><use href="#i-ext"/></svg></div><div class="tab-l">Extensions</div></div>
          <div class="tab"><div class="tab-iw"><svg><use href="#i-lib"/></svg></div><div class="tab-l">Library</div></div>
          <div class="tab"><div class="tab-iw"><svg><use href="#i-contacts"/></svg></div><div class="tab-l">Contacts</div></div>
          <div class="tab active"><div class="tab-iw"><svg><use href="#i-home"/></svg></div><div class="tab-l">Home</div></div>
        </div>
      </div>
    </div>

    <div class="variant-wrap">
      <div class="variant-lbl blue">Pro org · new or few chats · straight into setup</div>
      <div class="phone">
        <div class="sb"><span class="sb-t">10:20</span><div class="sb-r">●●● 🔋</div></div>
        <div class="hh"><div class="hh-ic"><svg><use href="#i-gear"/></svg></div><div class="hh-ic"><svg><use href="#i-search"/></svg></div><div class="hh-pill"><span class="hh-name">Pizza Yoav</span><div class="hh-av" style="background:linear-gradient(135deg,#E05A1C,#B83A10)">PY</div></div></div>
        <div class="ftabs"><div class="fp on">Chats</div><div class="fp">★ Starred</div><div class="fp">Unread</div></div>
        <div style="background:#F8F8F8;padding-bottom:8px">
          <div class="nudge blue">
            <div class="nudge-x">✕</div>
            <span class="nudge-icon">🏢</span>
            <div class="nudge-title">Your team is growing</div>
            <div class="nudge-body">Your workspace just crossed 20 members. Set up Teams & Locations so the right people talk to the right people.</div>
            <div class="nudge-btn blue" onclick="nextPage()">Set up now →</div>
          </div>
          <div class="crow"><div class="cav-r" style="background:#FFF3E0">👨‍🍳</div><div class="ci"><div class="cn">Kitchen Team</div><div class="cp">✨ Created by Zenzap AI</div></div><div class="cm"><div class="ct">Jun 3</div></div></div>
          <div class="crow"><div class="cav-r" style="background:#E3F2FD">📅</div><div class="ci"><div class="cn">Work Schedule</div><div class="cp">Shift update from manager</div></div><div class="cm"><div class="ct">Jun 3</div></div></div>
        </div>
        <div class="tabbar">
          <div class="tab"><div class="tab-iw"><svg><use href="#i-admin"/></svg></div><div class="tab-l">Admin</div></div>
          <div class="tab"><div class="tab-iw"><svg><use href="#i-ext"/></svg></div><div class="tab-l">Extensions</div></div>
          <div class="tab"><div class="tab-iw"><svg><use href="#i-lib"/></svg></div><div class="tab-l">Library</div></div>
          <div class="tab"><div class="tab-iw"><svg><use href="#i-contacts"/></svg></div><div class="tab-l">Contacts</div></div>
          <div class="tab active"><div class="tab-iw"><svg><use href="#i-home"/></svg></div><div class="tab-l">Home</div></div>
        </div>
      </div>
    </div>

    <div class="variant-wrap">
      <div class="variant-lbl amber">Pro org · existing chats · needs sorting (or resume)</div>
      <div class="phone">
        <div class="sb"><span class="sb-t">10:20</span><div class="sb-r">●●● 🔋</div></div>
        <div class="hh"><div class="hh-ic"><svg><use href="#i-gear"/></svg></div><div class="hh-ic"><svg><use href="#i-search"/></svg></div><div class="hh-pill"><span class="hh-name">Pizza Yoav</span><div class="hh-av" style="background:linear-gradient(135deg,#E05A1C,#B83A10)">PY</div></div></div>
        <div class="ftabs"><div class="fp on">Chats</div><div class="fp">★ Starred</div><div class="fp">Unread</div></div>
        <div style="background:#F8F8F8;padding-bottom:8px">
          <div class="nudge amber">
            <div class="nudge-x">✕</div>
            <span class="nudge-icon">📋</span>
            <div class="nudge-title">Organize your existing chats</div>
            <div class="nudge-body">You have 6 chats. No history lost — set up Teams & Locations to control who sees what.</div>
            <div class="nudge-prog"><div class="nudge-prog-bar"><div class="nudge-prog-fill" style="width:0%;background:#F5A623"></div></div><div class="nudge-prog-lbl" style="color:#F5A623">Not started</div></div>
            <div class="nudge-btn amber" onclick="nextPage()">Start setup →</div>
          </div>
          <div class="crow"><div class="cav-r" style="background:#FFF3E0">👨‍🍳</div><div class="ci"><div class="cn">Kitchen — All Branches</div><div class="cp">Ali: New prep schedule</div></div><div class="cm"><div class="ct">Jun 3</div><div class="cbadge">4</div></div></div>
          <div class="crow"><div class="cav-r" style="background:#E3F2FD">🍷</div><div class="ci"><div class="cn">Waiters Group</div><div class="cp">Shift starts 18:00 today</div></div><div class="cm"><div class="ct">Jun 3</div></div></div>
        </div>
        <div class="tabbar">
          <div class="tab"><div class="tab-iw"><svg><use href="#i-admin"/></svg></div><div class="tab-l">Admin</div></div>
          <div class="tab"><div class="tab-iw"><svg><use href="#i-ext"/></svg></div><div class="tab-l">Extensions</div></div>
          <div class="tab"><div class="tab-iw"><svg><use href="#i-lib"/></svg></div><div class="tab-l">Library</div></div>
          <div class="tab"><div class="tab-iw"><svg><use href="#i-contacts"/></svg></div><div class="tab-l">Contacts</div></div>
          <div class="tab active"><div class="tab-iw"><svg><use href="#i-home"/></svg></div><div class="tab-l">Home</div></div>
        </div>
      </div>
    </div>

  </div>
  <div class="ann"><div class="ann-dot"></div><div class="ann-txt"><strong>Three nudges, four entry points.</strong> <strong>Orange (Free → paywall):</strong> same 20-member threshold, but the CTA leads to a pricing screen first — completing the upgrade drops directly into Step 1, so setup is part of the migration to paid. <strong>Blue (Pro, new):</strong> few or no existing chats, straight into the wizard; Step 2 (Industry) asked from scratch; Step 4 may be sparse or empty — "Skip for now" saves the structure and re-surfaces assignment when members join. <strong>Amber (Pro, existing):</strong> existing flat chats that Step 5 will sort; Step 2 is pre-filled from workspace signals (channel names, prior input), admin can change; Step 4 has a full member list. <strong>Incomplete setup re-surface:</strong> the amber nudge reappears with a progress bar showing how far the admin got — tapping it resumes at the last incomplete step, not Step 1.</div></div>
</div>

<!-- PAGE 2 — Screen 2: Step 1, Locations (single phone, toggle switches view) -->
<div class="sg page" data-page="2">
  <div class="sg-n">Screen 2 · 8</div>
  <div class="sg-t">Wizard — Step 1 · Locations, with a "multiple locations" toggle</div>
  <div class="hint">↑ Tap the toggle to switch views · add, edit, or remove locations</div>
  <div class="phone">
    <div class="sb"><span class="sb-t">10:22</span><div class="sb-r">●●● 🔋</div></div>
    <div class="nb"><div class="nb-back" onclick="prevPage()"><svg><use href="#i-chevl"/></svg></div><div class="nb-title">Teams & Locations</div><div class="nb-sp"></div></div>
    <div class="wprog"><div class="ws now"></div><div class="ws next"></div><div class="ws next"></div><div class="ws next"></div><div class="ws next"></div></div>
    <div style="background:#fff" class="loc-toggle-wrap">
      <div class="wb">
        <div class="wstep">Step 1 of 5</div>
        <div class="wtitle">Where do you operate?</div>
        <div class="wsub loc-sub">Single site — you can switch this on anytime in Settings.</div>
      </div>
      <div class="srow" style="padding:12px 18px">
        <div><div class="srow-l" style="font-size:14px;font-weight:600">Multiple locations</div><div class="srow-l2">This workspace operates from more than one site</div></div>
        <div class="tog off" onclick="toggleLoc(this)"></div>
      </div>
      <div class="loc-off-content">
        <div class="loc-input-row"><div class="loc-dot"></div><input class="loc-input" value="Pizza Yoav"><div class="loc-del" style="visibility:hidden">✕</div></div>
      </div>
      <div class="loc-on-content" style="display:none">
        <div id="locList">
          <div class="loc-input-row"><div class="loc-dot"></div><input class="loc-input" value="Tel Aviv"><div class="loc-del" onclick="this.closest('.loc-input-row').remove()">✕</div></div>
          <div class="loc-input-row"><div class="loc-dot"></div><input class="loc-input" value="Herzliya"><div class="loc-del" onclick="this.closest('.loc-input-row').remove()">✕</div></div>
        </div>
        <div class="loc-add-row" onclick="addLocation()">
          <div style="font-size:18px">＋</div>
          <div class="loc-add-txt">Add another location</div>
        </div>
      </div>
    </div>
    <div style="padding:14px 18px 20px;background:#fff"><div class="btn-p" onclick="nextPage()">Next →</div></div>
    <div class="tabbar">
      <div class="tab active"><div class="tab-iw"><svg><use href="#i-admin"/></svg></div><div class="tab-l">Admin</div></div>
      <div class="tab"><div class="tab-iw"><svg><use href="#i-ext"/></svg></div><div class="tab-l">Extensions</div></div>
      <div class="tab"><div class="tab-iw"><svg><use href="#i-lib"/></svg></div><div class="tab-l">Library</div></div>
      <div class="tab"><div class="tab-iw"><svg><use href="#i-contacts"/></svg></div><div class="tab-l">Contacts</div></div>
      <div class="tab"><div class="tab-iw"><svg><use href="#i-home"/></svg></div><div class="tab-l">Home</div></div>
    </div>
  </div>
  <div class="ann"><div class="ann-dot"></div><div class="ann-txt"><strong>One toggle, off by default, instead of a separate setup question.</strong> Off: a single field pre-filled with the workspace name (editable) — Next is immediately available, no extra step. On: reveals an editable add/remove list — type to rename, ✕ to remove, "+ Add another location" to append. Every downstream step (industry, teams, org structure, assign, review) is identical either way — Team × Location stays the universal permission key even when there's only one location. Toggle remains editable later in Settings, so a single-site org that opens a second branch doesn't need to redo setup.</div></div>
</div>

<!-- PAGE 3 — Screen 3: Step 2, Industry & Teams -->
<div class="sg page" data-page="3">
  <div class="sg-n">Screen 3 · 8</div>
  <div class="sg-t">Wizard — Step 2 · Industry & teams</div>
  <div class="hint">↑ Tap a different industry — suggested teams update</div>
  <div class="phone full">
    <div class="sb"><span class="sb-t">10:24</span><div class="sb-r">●●● 🔋</div></div>
    <div class="nb"><div class="nb-back" onclick="prevPage()"><svg><use href="#i-chevl"/></svg></div><div class="nb-title">Teams & Locations</div><div class="nb-sp"></div></div>
    <div class="wprog"><div class="ws done"></div><div class="ws now"></div><div class="ws next"></div><div class="ws next"></div><div class="ws next"></div></div>
    <div style="background:#fff;padding-bottom:16px">
      <div class="wb">
        <div class="wstep">Step 2 of 5</div>
        <div class="wtitle">What kind of business?</div>
        <div class="wsub">We'll suggest the right teams for your industry.</div>
        <div style="background:#FFFBEE;border:1px solid rgba(245,166,35,.25);border-radius:10px;padding:9px 12px;margin-bottom:12px;font-size:12px;color:#7A5200;display:flex;align-items:center;justify-content:space-between;gap:8px">
          <span>✨ Pre-filled based on your existing channels</span>
          <span style="font-size:11px;font-weight:700;color:#F5A623;white-space:nowrap">Change ▾</span>
        </div>
        <div class="igrid">
          <div class="icard sel" data-industry="Restaurant" onclick="selectIndustry(this)"><div class="icard-icon">🍽️</div><div class="icard-lbl">Restaurant</div></div>
          <div class="icard" data-industry="Hotel" onclick="selectIndustry(this)"><div class="icard-icon">🏨</div><div class="icard-lbl">Hotel</div></div>
          <div class="icard" data-industry="Retail" onclick="selectIndustry(this)"><div class="icard-icon">🛍️</div><div class="icard-lbl">Retail</div></div>
          <div class="icard" data-industry="Healthcare" onclick="selectIndustry(this)"><div class="icard-icon">🏥</div><div class="icard-lbl">Healthcare</div></div>
          <div class="icard" data-industry="Construction" onclick="selectIndustry(this)"><div class="icard-icon">🏗️</div><div class="icard-lbl">Construction</div></div>
          <div class="icard" data-industry="Other" onclick="selectIndustry(this)" style="border:2px dashed #D8D8D8;background:#FAFAFA"><div class="icard-icon" style="font-size:17px;color:#BBB">＋</div><div class="icard-lbl" style="color:#BBB">Other</div></div>
        </div>
        <div class="aicard">
          <div class="aihdr">
            <div class="aibadge">AI</div>
            <div class="ait">Suggested teams</div>
          </div>
          <div class="chips" id="teamChips">
            <div class="chip">👨‍🍳 Kitchen <span class="chip-scope">· location</span><span class="chip-x">✕</span></div>
            <div class="chip">🍷 Waiters <span class="chip-scope">· location</span><span class="chip-x">✕</span></div>
            <div class="chip">💼 Management <span class="chip-scope">· all</span><span class="chip-x">✕</span></div>
            <div class="chip">🧹 Cleaning <span class="chip-scope">· location</span><span class="chip-x">✕</span></div>
            <div class="chip-add">＋ Add</div>
          </div>
        </div>
        <div class="btn-p" onclick="nextPage()">Next →</div>
      </div>
    </div>
    <div class="tabbar">
      <div class="tab active"><div class="tab-iw"><svg><use href="#i-admin"/></svg></div><div class="tab-l">Admin</div></div>
      <div class="tab"><div class="tab-iw"><svg><use href="#i-ext"/></svg></div><div class="tab-l">Extensions</div></div>
      <div class="tab"><div class="tab-iw"><svg><use href="#i-lib"/></svg></div><div class="tab-l">Library</div></div>
      <div class="tab"><div class="tab-iw"><svg><use href="#i-contacts"/></svg></div><div class="tab-l">Contacts</div></div>
      <div class="tab"><div class="tab-iw"><svg><use href="#i-home"/></svg></div><div class="tab-l">Home</div></div>
    </div>
  </div>
  <div class="ann"><div class="ann-dot"></div><div class="ann-txt"><strong>Clean and focused.</strong> One question: what's your business? AI generates team chips immediately on selection, and the suggestions change per industry — a Hotel gets Front Desk/Housekeeping, a Clinic gets Nursing/Reception. Scope tag (· location / · all) tells admin whether a team is location-scoped or org-wide — no permission language, just scope. Admin's only job: is this the right list of teams?</div></div>
</div>

<!-- PAGE 4 — Screen 4: Step 3, Org Structure -->
<div class="sg page" data-page="4">
  <div class="sg-n">Screen 4 · 8</div>
  <div class="sg-t">Wizard — Step 3 · Org structure + permission hints</div>
  <div class="hint">↑ Drag ⠿ to reorder · ＋ to add · ✕ to remove · Rename to edit, then Save</div>
  <div class="phone">
    <div class="sb"><span class="sb-t">10:26</span><div class="sb-r">●●● 🔋</div></div>
    <div class="nb"><div class="nb-back" onclick="prevPage()"><svg><use href="#i-chevl"/></svg></div><div class="nb-title">Teams & Locations</div><div class="nb-sp"></div></div>
    <div class="wprog"><div class="ws done"></div><div class="ws done"></div><div class="ws now"></div><div class="ws next"></div><div class="ws next"></div></div>
    <div style="background:#fff;padding-bottom:16px">
      <div class="wb">
        <div class="wstep">Step 3 of 5</div>
        <div class="wtitle">Your org structure</div>
        <div class="wsub">Based on Restaurant — fully customizable.</div>
      </div>

      <div class="tier-editor">
        <div class="tier-hdr">
          <div class="tier-badge">AI</div>
          <div class="tier-title">Role hierarchy</div>
        </div>
        <div class="tier-summary" id="tierSummary"></div>
        <div class="cust-toggle" onclick="toggleCustomize(this)" id="custToggle">▾ Customize hierarchy</div>
        <div class="cust-editor" id="custEditor">
          <div class="tier-rows" id="tierRows"></div>
          <div class="tier-add" id="tierAddBtn" onclick="addTier()">＋ Add a tier</div>
        </div>
      </div>

      <div class="div-lbl"><div class="div-line"></div><div class="div-txt">Communication Boundaries</div><div class="div-line"></div></div>

      <div class="bound-card">
        <div class="bound-hdr">
          <div><div class="bound-title">Restrict messaging across teams</div><div class="bound-sub">Same location, different team</div></div>
          <div class="tog off" onclick="toggleBoundary(this,'team')"></div>
        </div>
        <div class="bound-list" id="teamOpenList">
          <div class="bound-item">✓ Members can message peers on any team at this location</div>
          <div class="bound-item">✓ One level up (their manager) is unaffected</div>
        </div>
        <div class="bound-list" id="teamRestrictList" style="display:none">
          <div class="bound-item neg">✕ Members can only message within their own team</div>
          <div class="bound-item neg">✕ Existing cross-team chats stay active, but closed to new members</div>
        </div>
        <div class="bound-exception" id="teamException" style="display:none">
          <div class="bound-exception-lbl">Who's exempt from this restriction?</div>
          <div class="bound-radio sel" onclick="selectException(this)"><span class="bound-radio-dot"></span><span class="exc-label-1">Shift Lead and above</span></div>
          <div class="bound-radio" onclick="selectException(this)"><span class="bound-radio-dot"></span><span>Org Admin only</span></div>
        </div>
      </div>

      <div class="bound-card">
        <div class="bound-hdr">
          <div><div class="bound-title">Restrict messaging across locations</div><div class="bound-sub">Different branch, same org</div></div>
          <div class="tog on" onclick="toggleBoundary(this,'loc')"></div>
        </div>
        <div class="bound-list" id="locRestrictList">
          <div class="bound-item neg">✕ Members can only message contacts at their own location</div>
        </div>
        <div class="bound-list" id="locOpenList" style="display:none">
          <div class="bound-item">✓ Members can message peers at any location</div>
        </div>
        <div class="bound-exception" id="locException">
          <div class="bound-exception-lbl">Who's exempt from this restriction?</div>
          <div class="bound-radio sel" onclick="selectException(this)"><span class="bound-radio-dot"></span><span>Org Admin only</span></div>
          <div class="bound-radio" onclick="selectException(this)"><span class="bound-radio-dot"></span><span class="exc-label-1">Shift Lead and above</span></div>
        </div>
      </div>

      <div style="padding:0 18px 0"><div class="btn-p" onclick="nextPage()">Next →</div></div>
    </div>
    <div class="tabbar">
      <div class="tab active"><div class="tab-iw"><svg><use href="#i-admin"/></svg></div><div class="tab-l">Admin</div></div>
      <div class="tab"><div class="tab-iw"><svg><use href="#i-ext"/></svg></div><div class="tab-l">Extensions</div></div>
      <div class="tab"><div class="tab-iw"><svg><use href="#i-lib"/></svg></div><div class="tab-l">Library</div></div>
      <div class="tab"><div class="tab-iw"><svg><use href="#i-contacts"/></svg></div><div class="tab-l">Contacts</div></div>
      <div class="tab"><div class="tab-iw"><svg><use href="#i-home"/></svg></div><div class="tab-l">Home</div></div>
    </div>
  </div>
  <div class="ann"><div class="ann-dot"></div><div class="ann-txt"><strong>Hints are computed from rank and neighbors, not typed or looked up by name.</strong> Drag a tier and its hint — and its neighbors' hints — recompute on drop: the top custom tier always "sees all branches · can message anyone," the bottom always "sees their team only," and anything in between "sees their team · can reach [the tier above]." Add a tier and it drops in as an editable slot, ready to be named and <strong>Saved</strong>; remove one with ✕ (the bottom tier is protected). Whatever changed gets a highlight — no other indicator needed. <strong>Communication Boundaries</strong>, below the hierarchy, mirrors Zenzap's existing "Restrict communication by team" pattern — a restriction toggle, a plain-language "what this means" list, and a "who's exempt" choice — applied to both axes. <strong>Cross-team</strong> starts unrestricted (today's default: members can reach any team at their location, one level up unaffected); restricting it falls back to Zenzap's own behavior — existing mixed chats stay active but closed to new members, not frozen. <strong>Cross-location</strong> starts restricted (today's default), exempting only Org Admin; switching the exemption to "<span class="exc-label-1">Shift Lead and above</span>" is the Cross-Location Modifier from the doc — and that name updates live from whatever Step 3's second tier is called. <strong>Note: the full drag-and-drop tier editor is a v2 capability.</strong> In v1, the default 5-tier hierarchy ships as-is; "Customize hierarchy ▾" is present but scoped to name editing only. Full reordering, add/remove, and live hint recomputation ship after validating that admins need it.</div></div>
</div>

<!-- PAGE 5 — Screen 5: Step 4, Assign -->
<div class="sg page" data-page="5">
  <div class="sg-n">Screen 5 · 8</div>
  <div class="sg-t">Wizard — Step 4 · Assign members, with checkbox bulk-assign</div>
  <div class="hint">↑ Pills are dropdowns · check 2+ rows, set the bulk bar's Team/Location, Apply</div>
  <div class="phone full">
    <div class="sb"><span class="sb-t">10:29</span><div class="sb-r">●●● 🔋</div></div>
    <div class="nb"><div class="nb-back" onclick="prevPage()"><svg><use href="#i-chevl"/></svg></div><div class="nb-title">Assign Members</div><div class="nb-sp"></div></div>
    <div class="wprog"><div class="ws done"></div><div class="ws done"></div><div class="ws done"></div><div class="ws now"></div><div class="ws next"></div></div>
    <div style="background:#F8F8F8;padding-bottom:14px">
      <div style="padding:14px 18px 10px;background:#fff;border-bottom:.5px solid #F2F2F2">
        <div class="wstep">Step 4 of 5</div>
        <div class="wtitle">Assign your team</div>
        <div style="font-size:13px;color:#AAA">Set each person's team and location. Editable anytime.</div>
        <div style="display:flex;gap:6px;margin-top:10px">
          <div id="tab-populated" onclick="switchAssignState('populated')" style="flex:1;text-align:center;padding:6px 0;border-radius:8px;font-size:12px;font-weight:700;cursor:pointer;background:#4A6CF7;color:#fff">Existing org</div>
          <div id="tab-empty" onclick="switchAssignState('empty')" style="flex:1;text-align:center;padding:6px 0;border-radius:8px;font-size:12px;font-weight:700;cursor:pointer;background:#F0F0F0;color:#888">New / empty org</div>
        </div>
      </div>
      <div style="background:#fff;border-bottom:.5px solid #F2F2F2">
        <div class="delegate-bar" style="margin-bottom:10px">
          <div class="delegate-ic">👥</div>
          <div class="delegate-t">
            <div class="delegate-title">Let managers assign their own branches</div>
            <div class="delegate-sub">Send invite to each Regional Manager →</div>
          </div>
          <div class="delegate-btn">Delegate</div>
        </div>
      </div>

      <!-- Empty state panel -->
      <div id="assignEmptyState" style="display:none;padding:32px 24px;text-align:center;background:#fff;margin-top:10px">
        <div style="font-size:36px;margin-bottom:12px">👥</div>
        <div style="font-size:15px;font-weight:700;color:#000;margin-bottom:6px">No members yet</div>
        <div style="font-size:13px;color:#AAA;line-height:1.5;margin-bottom:20px">Invite your team first, then come back to assign them. Your org structure is already saved.</div>
        <div style="display:flex;flex-direction:column;gap:8px;padding:0 8px">
          <div class="btn-p" onclick="nextPage()">Skip for now — invite team first</div>
          <div class="csv-bar"><div style="font-size:16px">📄</div><div class="csv-t">Or import members from CSV</div><div class="csv-btn">Upload ↑</div></div>
        </div>
        <div style="font-size:11px;color:#C8C8C8;margin-top:14px">You'll be reminded to finish setup when your team joins.</div>
      </div>
      <div id="assignPopulatedState">
        <div style="background:#fff;margin-top:10px">
          <div class="brow"><div class="bav" style="background:linear-gradient(135deg,#4A6CF7,#2451C4)">YA</div><div class="bname">Yoav A.</div><div class="bdds" id="pills-yoav"></div></div>
          <div class="brow"><div class="bav" style="background:linear-gradient(135deg,#FF6B6B,#C0392B)">MK</div><div class="bname">Maya K.</div><div class="bdds" id="pills-maya"></div></div>
          <div class="brow"><div class="bav" style="background:linear-gradient(135deg,#48C774,#2E7D32)">DL</div><div class="bname">Dani L.</div><div class="bdds" id="pills-dani"></div></div>
          <div class="brow"><div class="bav" style="background:linear-gradient(135deg,#FFAA00,#F57F17)">RP</div><div class="bname">Rina P.</div><div class="bdds" id="pills-rina"></div></div>
          <div class="brow"><div class="bav" style="background:linear-gradient(135deg,#AB47BC,#6A1B9A)">BS</div><div class="bname">Ben S.</div><div class="bdds" id="pills-ben"></div></div>
          <div class="brow"><div class="bav" style="background:linear-gradient(135deg,#26C6DA,#00838F)">NB</div><div class="bname">Noa B.</div><div class="bdds" id="pills-noa"></div></div>
          <div class="bulk-toggle" onclick="toggleBulkSection(this)">▾ Bulk actions</div>
          <div class="bulk-section" id="bulkSection">
            <div class="bulk-bar" id="bulkBar" style="display:none">
              <div class="bulk-top"><span class="bulk-count" id="bulkCount">2 selected</span><span class="bulk-clear" onclick="bulkClear()">✕ Clear</span></div>
              <div class="bulk-row">
                <select id="bulkTeam" class="bulk-pill-select">
                  <option value="Waiters" selected>Waiters</option>
                  <option value="Kitchen">Kitchen</option>
                  <option value="Mgmt">Mgmt</option>
                  <option value="Cleaning">Cleaning</option>
                </select>
                <select id="bulkLoc" class="bulk-pill-select">
                  <option value="TLV" selected>Tel Aviv</option>
                  <option value="HRZ">Herzliya</option>
                </select>
                <span class="bulk-apply" onclick="bulkApply()">Apply</span>
              </div>
              <div class="bulk-note">Adds to each member's current assignment — won't remove what they already have.</div>
            </div>
            <div style="background:#fff">
              <div class="brow"><div class="bchk" data-member="yoav" onclick="toggleChk(this)"></div><div class="bav" style="background:linear-gradient(135deg,#4A6CF7,#2451C4)">YA</div><div class="bname">Yoav A.</div><div class="bdds" id="bulk-pills-yoav"></div></div>
              <div class="brow"><div class="bchk" data-member="maya" onclick="toggleChk(this)"></div><div class="bav" style="background:linear-gradient(135deg,#FF6B6B,#C0392B)">MK</div><div class="bname">Maya K.</div><div class="bdds" id="bulk-pills-maya"></div></div>
              <div class="brow"><div class="bchk" data-member="dani" onclick="toggleChk(this)"></div><div class="bav" style="background:linear-gradient(135deg,#48C774,#2E7D32)">DL</div><div class="bname">Dani L.</div><div class="bdds" id="bulk-pills-dani"></div></div>
              <div class="brow"><div class="bchk" data-member="rina" onclick="toggleChk(this)"></div><div class="bav" style="background:linear-gradient(135deg,#FFAA00,#F57F17)">RP</div><div class="bname">Rina P.</div><div class="bdds" id="bulk-pills-rina"></div></div>
              <div class="brow"><div class="bchk" data-member="ben" onclick="toggleChk(this)"></div><div class="bav" style="background:linear-gradient(135deg,#AB47BC,#6A1B9A)">BS</div><div class="bname">Ben S.</div><div class="bdds" id="bulk-pills-ben"></div></div>
              <div class="brow"><div class="bchk" data-member="noa" onclick="toggleChk(this)"></div><div class="bav" style="background:linear-gradient(135deg,#26C6DA,#00838F)">NB</div><div class="bname">Noa B.</div><div class="bdds" id="bulk-pills-noa"></div></div>
            </div>
            <div style="padding:9px 14px 0"><div class="csv-bar"><div style="font-size:16px">📄</div><div class="csv-t">Import from CSV for large teams</div><div class="csv-btn">Upload ↑</div></div></div>
          </div>
        </div>
        <div style="padding:9px 14px 0"><div class="btn-p" onclick="nextPage()">Next: Review changes →</div></div>
      </div>
    </div>
    <div class="tabbar">
      <div class="tab active"><div class="tab-iw"><svg><use href="#i-admin"/></svg></div><div class="tab-l">Admin</div></div>
      <div class="tab"><div class="tab-iw"><svg><use href="#i-ext"/></svg></div><div class="tab-l">Extensions</div></div>
      <div class="tab"><div class="tab-iw"><svg><use href="#i-lib"/></svg></div><div class="tab-l">Library</div></div>
      <div class="tab"><div class="tab-iw"><svg><use href="#i-contacts"/></svg></div><div class="tab-l">Contacts</div></div>
      <div class="tab"><div class="tab-iw"><svg><use href="#i-home"/></svg></div><div class="tab-l">Home</div></div>
    </div>
  </div>
  <div class="ann"><div class="ann-dot"></div><div class="ann-txt"><strong>Two states, one screen.</strong> Toggle the tabs above to see both. <strong>Existing org:</strong> full member list, dropdown pills per row, "Bulk actions ▾" for checkboxes + batch apply + CSV, Delegate for large multi-location orgs. <strong>New / empty org:</strong> no member list to show — rather than an empty table with a confusing CSV-only path, the screen surfaces the situation honestly and offers a clean exit. Org structure is already saved; a persistent nudge in My Company re-surfaces Step 4 when members join. CSV import stays available for orgs who onboard via spreadsheet from day one. <strong>Apply is always additive</strong> — bulk-applying Waiters·TLV to Maya (already Kitchen·TLV) adds a second team without removing her first; her pill becomes "2 teams."</div></div>
</div>

<!-- PAGE 6 — Screen 6: Step 5, Review & Activate -->
<div class="sg page" data-page="6">
  <div class="sg-n">Screen 6 · 8</div>
  <div class="sg-t">Wizard — Step 5 · Review & activate</div>
  <div class="hint">↑ Tap Activate for the confirmation toast</div>
  <div class="phone full">
    <div class="sb"><span class="sb-t">10:32</span><div class="sb-r">●●● 🔋</div></div>
    <div class="nb"><div class="nb-back" onclick="prevPage()"><svg><use href="#i-chevl"/></svg></div><div class="nb-title">Review Changes</div><div class="nb-sp"></div></div>
    <div class="wprog"><div class="ws done"></div><div class="ws done"></div><div class="ws done"></div><div class="ws done"></div><div class="ws now"></div></div>
    <div style="background:#F8F8F8;padding-bottom:16px">
      <div style="padding:14px 18px 10px;background:#fff;border-bottom:.5px solid #F2F2F2">
        <div class="wstep">Step 5 of 5</div>
        <div class="wtitle">Here's what will change</div>
        <div style="font-size:13px;color:#AAA">Nothing changes until you tap Activate.</div>
      </div>
      <div style="height:6px"></div>
      <div style="background:#fff">
        <div class="trow"><div class="ticon" style="background:#FFF3E0">👨‍🍳</div><div class="tinfo"><div class="tname">Kitchen — All Branches</div><div class="tchange" style="color:#D32F2F">→ Split by location · Kitchen only</div></div><div class="tbadge badge-r">Restricted</div></div>
        <div class="trow"><div class="ticon" style="background:#FFF3E0">🍷</div><div class="tinfo"><div class="tname">Waiters Group</div><div class="tchange" style="color:#D32F2F">→ Waiters · Tel Aviv only</div></div><div class="tbadge badge-r">Restricted</div></div>
        <div class="trow"><div class="ticon" style="background:#F3E5F5">📢</div><div class="tinfo"><div class="tname">Company News</div><div class="tchange" style="color:#2E7D32">→ Stays visible to everyone</div></div><div class="tbadge badge-g">Open</div></div>
        <div class="trow"><div class="ticon" style="background:#E3F2FD">💼</div><div class="tinfo"><div class="tname">Management</div><div class="tchange" style="color:#888">→ No change</div></div><div class="tbadge badge-gr">Unchanged</div></div>
        <div class="trow"><div class="ticon" style="background:#F0F0F0">📦</div><div class="tinfo"><div class="tname">All Staff (47, imported from WhatsApp)</div><div class="tchange" style="color:#999">→ Becomes read-only · history kept</div></div><div class="tbadge badge-legacy">Legacy</div></div>
      </div>
      <div class="warnbar">⚠️ <strong>Nothing is deleted.</strong> Message history is preserved for every chat, including those marked Legacy.</div>
      <div style="padding:0 14px;display:flex;flex-direction:column;gap:8px">
        <div class="btn-p" onclick="activate()">Activate Teams & Locations</div>
        <div class="btn-s" onclick="prevPage()">Go back and edit</div>
      </div>
    </div>
    <div class="tabbar">
      <div class="tab active"><div class="tab-iw"><svg><use href="#i-admin"/></svg></div><div class="tab-l">Admin</div></div>
      <div class="tab"><div class="tab-iw"><svg><use href="#i-ext"/></svg></div><div class="tab-l">Extensions</div></div>
      <div class="tab"><div class="tab-iw"><svg><use href="#i-lib"/></svg></div><div class="tab-l">Library</div></div>
      <div class="tab"><div class="tab-iw"><svg><use href="#i-contacts"/></svg></div><div class="tab-l">Contacts</div></div>
      <div class="tab"><div class="tab-iw"><svg><use href="#i-home"/></svg></div><div class="tab-l">Home</div></div>
    </div>
  </div>
  <div class="ann"><div class="ann-dot"></div><div class="ann-txt"><strong>The migration moment.</strong> Every existing chat listed with its outcome. Nothing changes silently. <strong>"Legacy"</strong> is a fourth outcome alongside Restricted / Open / Unchanged — for flat WhatsApp-imported groups that don't map onto the new Team × Location structure. Rather than silently removing people from a chat they recognize, Zenzap freezes it as read-only: full history stays visible to original members, no new posts or membership changes. Go-forward communication happens in the new scoped channels above. <strong>Activate</strong> shows a brief confirmation toast — non-blocking, mobile-appropriate — rather than a modal the admin has to dismiss, then drops them straight into My Company (Screen 7) to see the result.</div></div>
</div>

<!-- PAGE 7 — Screen 7: My Company (post-setup) -->
<div class="sg page" data-page="7">
  <div class="sg-n">Screen 7 · 8</div>
  <div class="sg-t">My Company — post-setup management + sort sheet</div>
  <div class="hint">↑ Tap filter pills to toggle · tap "Unassigned first" to sort · tap Assign on Rina</div>
  <div class="phone full" style="position:relative">
    <div class="sb"><span class="sb-t">10:36</span><div class="sb-r">●●● 🔋</div></div>
    <div class="nb"><div class="nb-back" onclick="prevPage()"><svg><use href="#i-chevl"/></svg></div><div class="nb-title">My Company</div><div style="font-size:13px;color:#4A6CF7;font-weight:600">+ Add</div></div>
    <div style="background:#F8F8F8;padding-bottom:4px">
      <div style="padding:10px 14px 8px;background:#fff;border-bottom:.5px solid #F2F2F2">
        <div style="background:#F0F0F0;border-radius:9px;padding:8px 12px;display:flex;align-items:center;gap:7px;margin-bottom:8px">
          <svg width="13" height="13" viewBox="0 0 24 24" fill="none"><circle cx="11" cy="11" r="8" stroke="#AAA" stroke-width="2"/><line x1="21" y1="21" x2="16.65" y2="16.65" stroke="#AAA" stroke-width="2" stroke-linecap="round"/></svg>
          <span style="font-size:13px;color:#BBB">Search</span>
        </div>
        <div style="display:flex;gap:6px;overflow-x:auto;padding-bottom:4px">
          <div class="fp on" onclick="this.classList.toggle('on')">Team ▾</div>
          <div class="fp" onclick="this.classList.toggle('on')">Location ▾</div>
          <div class="fp" onclick="this.classList.toggle('on')">Role ▾</div>
          <div class="fp" onclick="this.classList.toggle('on')">Status ▾</div>
        </div>
        <div style="display:flex;align-items:center;justify-content:space-between;padding-top:7px">
          <div style="font-size:11px;color:#C8C8C8">24 members</div>
          <div id="sortTrigger" onclick="openSort()" style="font-size:11px;font-weight:600;color:#555;background:#F0F0F0;border-radius:6px;padding:4px 8px;display:flex;align-items:center;gap:4px;cursor:pointer">
            <svg width="11" height="11" viewBox="0 0 24 24" fill="none"><line x1="3" y1="6" x2="21" y2="6" stroke="#666" stroke-width="2" stroke-linecap="round"/><line x1="6" y1="12" x2="18" y2="12" stroke="#666" stroke-width="2" stroke-linecap="round"/><line x1="10" y1="18" x2="14" y2="18" stroke="#666" stroke-width="2" stroke-linecap="round"/></svg>
            <span id="sortLabel">Unassigned first ▾</span>
          </div>
        </div>
      </div>
      <div class="ubar"><div class="ut" id="unassignedCount">⚠️ 2 members not yet assigned</div></div>
      <div style="background:#fff">
        <div class="mrow"><div class="mav" style="background:linear-gradient(135deg,#4A6CF7,#2451C4)">YA</div><div class="mi"><div class="mn">Yoav Avissara</div><div class="md">Admin · TLV, HRZ</div></div><div class="mchev">›</div></div>
        <div class="mrow"><div class="mav" style="background:linear-gradient(135deg,#FF6B6B,#C0392B)">MK</div><div class="mi"><div class="mn">Maya Koren</div><div class="md">Kitchen · Tel Aviv · Manager</div></div><div class="mchev">›</div></div>
        <div class="mrow"><div class="mav" style="background:linear-gradient(135deg,#48C774,#2E7D32)">DL</div><div class="mi"><div class="mn">Dani Levi</div><div class="md">Waiters · Herzliya · Shift Lead</div></div><div class="mchev">›</div></div>
        <div class="mrow"><div class="mav" style="background:linear-gradient(135deg,#FFAA00,#F57F17)">RP</div><div class="mi"><div class="mn">Rina Peretz</div><div class="md warn-t" id="rinaStatus">⚠ Not assigned</div></div><div class="assign-btn" id="rinaAssignBtn" onclick="assignRina()">Assign →</div></div>
        <div class="mrow"><div class="mav" style="background:linear-gradient(135deg,#AB47BC,#6A1B9A)">BS</div><div class="mi"><div class="mn">Ben Shapira</div><div class="md">Mgmt · TLV, HRZ · Manager</div></div><div class="mchev">›</div></div>
        <div class="mrow"><div class="mav" style="background:linear-gradient(135deg,#26C6DA,#00838F)">NB</div><div class="mi"><div class="mn">Noa Ben-David</div><div class="md">Waiters · Tel Aviv · Shift Lead</div></div><div class="mchev">›</div></div>
      </div>
      <div style="padding:9px 14px 4px"><div class="fab"><svg style="width:15px;height:15px"><use href="#i-person-add"/></svg> Add member</div></div>
    </div>
    <div class="tabbar">
      <div class="tab active"><div class="tab-iw"><svg><use href="#i-admin"/></svg></div><div class="tab-l">Admin</div></div>
      <div class="tab"><div class="tab-iw"><svg><use href="#i-ext"/></svg></div><div class="tab-l">Extensions</div></div>
      <div class="tab"><div class="tab-iw"><svg><use href="#i-lib"/></svg></div><div class="tab-l">Library</div></div>
      <div class="tab"><div class="tab-iw"><svg><use href="#i-contacts"/></svg></div><div class="tab-l">Contacts</div></div>
      <div class="tab"><div class="tab-iw"><svg><use href="#i-home"/></svg></div><div class="tab-l">Home</div></div>
    </div>

    <div class="sort-overlay" id="sortOverlay">
      <div class="sort-sheet">
        <div class="sort-handle"></div>
        <div class="sort-title">Sort by</div>
        <div class="sort-opts" id="sortOpts">
          <div class="sort-opt sel" onclick="selectSort(this)">Unassigned first <div class="sort-check">✓</div></div>
          <div class="sort-opt" onclick="selectSort(this)">Name A → Z <div class="sort-check">✓</div></div>
          <div class="sort-opt" onclick="selectSort(this)">Location <div class="sort-check">✓</div></div>
          <div class="sort-opt" onclick="selectSort(this)">Team <div class="sort-check">✓</div></div>
          <div class="sort-opt" onclick="selectSort(this)">Role level <div class="sort-check">✓</div></div>
        </div>
        <div style="padding:10px 14px 20px"><div class="btn-p" onclick="applySort()">Apply</div></div>
      </div>
    </div>
  </div>
  <div class="ann"><div class="ann-dot"></div><div class="ann-txt"><strong>Sort as a bottom sheet</strong> — native iOS/Android pattern, opens over the list on tap of the sort pill and closes on Apply, returning to the same screen with the new sort reflected in the pill's label. Filter pills (Team, Location, Role, Status) are independent toggles — no misleading "All" default. Unassigned members get an inline <strong>Assign →</strong> action right on their row — tapping it applies a default team/location the same way Step 4's bulk bar does, and the unassigned count drops accordingly. Unassigned warning always surfaced at top.</div></div>
</div>

<!-- PAGE 8 — Screen 8: Employee view -->
<div class="sg page" data-page="8">
  <div class="sg-n">Screen 8 · 8</div>
  <div class="sg-t">Employee view — single location vs. multi-location</div>
  <div class="variant-row">

    <div class="variant-wrap">
      <div class="variant-lbl" style="color:#555">Single location · Waiter · Tel Aviv</div>
      <div class="phone">
        <div class="sb"><span class="sb-t">10:45</span><div class="sb-r">●●● 🔋</div></div>
        <div class="emph"><div class="empw">Pizza Yoav</div><div class="locbadge">📍 Tel Aviv</div></div>
        <div class="ftabs"><div class="fp on">Chats</div><div class="fp">★ Starred</div><div class="fp">Unread</div></div>
        <div style="background:#F8F8F8">
          <div class="suprow">
            <div class="supav" style="background:linear-gradient(135deg,#26C6DA,#00838F)">NB</div>
            <div class="supi"><div class="supl">Your supervisor</div><div class="supn">Noa Ben-David</div></div>
            <div class="supmsg">Message</div>
          </div>
          <div class="seclbl">Your Chats</div>
          <div style="background:#fff">
            <div class="crow"><div class="cav-r" style="background:#FFF3E0">🍷</div><div class="ci"><div class="cn">Waiters · Tel Aviv</div><div class="cp">Noa: Shift starts 18:00 today</div></div><div class="cm"><div class="ct">10:12</div><div class="cbadge">3</div></div></div>
            <div class="crow"><div class="cav-r" style="background:#E8F5E9">📅</div><div class="ci"><div class="cn">Work Schedule · Tel Aviv</div><div class="cp">Updated for this week ✨</div></div><div class="cm"><div class="ct">09:45</div></div></div>
            <div class="crow"><div class="cav-r" style="background:#F3E5F5">📢</div><div class="ci"><div class="cn">Company News</div><div class="cp">New summer menu Monday</div></div><div class="cm"><div class="ct">Jun 10</div></div></div>
            <div class="crow"><div class="cav-c" style="background:linear-gradient(135deg,#48C774,#2E7D32)">DL</div><div class="ci"><div class="cn">Dani Levi</div><div class="cp">Can you cover Friday?</div></div><div class="cm"><div class="ct">Jun 9</div></div></div>
          </div>
        </div>
        <div class="tabbar">
          <div class="tab"><div class="tab-iw"><svg><use href="#i-admin"/></svg></div><div class="tab-l">Admin</div></div>
          <div class="tab"><div class="tab-iw"><svg><use href="#i-ext"/></svg></div><div class="tab-l">Extensions</div></div>
          <div class="tab"><div class="tab-iw"><svg><use href="#i-lib"/></svg></div><div class="tab-l">Library</div></div>
          <div class="tab"><div class="tab-iw"><svg><use href="#i-contacts"/></svg></div><div class="tab-l">Contacts</div></div>
          <div class="tab active"><div class="tab-iw"><svg><use href="#i-home"/></svg></div><div class="tab-l">Home</div></div>
        </div>
      </div>
    </div>

    <div class="variant-wrap">
      <div class="variant-lbl" style="color:#555">Multi-location · Nurse · 2 clinics</div>
      <div class="phone">
        <div class="sb"><span class="sb-t">10:45</span><div class="sb-r">●●● 🔋</div></div>
        <div class="emph"><div class="empw">Meridian Health</div><div class="locbadge">📍 2 locations</div></div>
        <div class="ftabs"><div class="fp on">Chats</div><div class="fp">★ Starred</div><div class="fp">Unread</div></div>
        <div style="background:#F8F8F8">
          <div class="suprow">
            <div class="supav" style="background:linear-gradient(135deg,#FF6B6B,#C0392B)">RS</div>
            <div class="supi"><div class="supl">Your supervisor</div><div class="supn">Dr. Roni Shapiro</div></div>
            <div class="supmsg">Message</div>
          </div>
          <div class="locsec">
            <div class="locname">📍 Tel Aviv Clinic <span class="loc-today">Today</span></div>
            <div class="loc-toggle">Collapse ↑</div>
          </div>
          <div style="background:#fff">
            <div class="crow"><div class="cav-r" style="background:#E3F2FD">🩺</div><div class="ci"><div class="cn">Dermatology · Tel Aviv</div><div class="cp">Dr. Cohen: Patient in room 3</div></div><div class="cm"><div class="ct">10:30</div><div class="cbadge">2</div></div></div>
            <div class="crow"><div class="cav-r" style="background:#E8F5E9">📅</div><div class="ci"><div class="cn">Schedule · Tel Aviv</div><div class="cp">Week updated</div></div><div class="cm"><div class="ct">09:00</div></div></div>
          </div>
          <div class="locsec" style="margin-top:3px">
            <div class="locname" style="color:#BBB">📍 Herzliya Clinic <span class="loc-next">Thu</span></div>
            <div class="loc-toggle">Expand ↓</div>
          </div>
          <div class="loc-coll"><div class="lc-name">2 chats · 1 unread</div></div>
        </div>
        <div class="tabbar">
          <div class="tab"><div class="tab-iw"><svg><use href="#i-admin"/></svg></div><div class="tab-l">Admin</div></div>
          <div class="tab"><div class="tab-iw"><svg><use href="#i-ext"/></svg></div><div class="tab-l">Extensions</div></div>
          <div class="tab"><div class="tab-iw"><svg><use href="#i-lib"/></svg></div><div class="tab-l">Library</div></div>
          <div class="tab"><div class="tab-iw"><svg><use href="#i-contacts"/></svg></div><div class="tab-l">Contacts</div></div>
          <div class="tab active"><div class="tab-iw"><svg><use href="#i-home"/></svg></div><div class="tab-l">Home</div></div>
        </div>
      </div>
    </div>

  </div>
  <div class="ann"><div class="ann-dot"></div><div class="ann-txt"><strong>No locked icons, no "not visible" cards.</strong> Single-location: focused channel list, peer DMs present, supervisor one tap away. Multi-location: today's clinic expanded, next clinic collapsed with unread count + day label. Both variants: employee experience feels curated, not restricted.</div></div>
</div>

<!-- PAGE 9 — Screen 9: Employee Contacts -->
<div class="sg page" data-page="9">
  <div class="sg-n">Screen 9 · 9</div>
  <div class="sg-t">Employee Contacts — two Cross-Team settings, same logic</div>
  <div class="hint">↑ Tap someone at another location · two phones show Cross-Team unrestricted vs. restricted</div>
  <div class="variant-row">

    <!-- LEFT: Cross-Team unrestricted (default) -->
    <div class="variant-wrap">
      <div class="variant-lbl blue">Cross-Team: unrestricted (default)</div>
      <div class="phone full">
        <div class="sb"><span class="sb-t">10:45</span><div class="sb-r">●●● 🔋</div></div>
        <div class="nb"><div class="nb-back" onclick="prevPage()"><svg><use href="#i-chevl"/></svg></div><div class="nb-title">Contacts</div><div class="nb-sp"></div></div>
        <div style="background:#F8F8F8;padding-bottom:8px">
          <div class="nudge blue">
            <div class="nudge-x" onclick="this.closest('.nudge').remove()">✕</div>
            <span class="nudge-icon">✨</span>
            <div class="nudge-title">What's new: Teams & Locations</div>
            <div class="nudge-body">Your workspace is now organized by team and location. You can message anyone on your team, plus other teams here at Tel Aviv. For other locations, message your supervisor and they'll connect you.</div>
          </div>
          <div class="suprow">
            <div class="supav" style="background:linear-gradient(135deg,#26C6DA,#00838F)">NB</div>
            <div class="supi"><div class="supl">Your supervisor</div><div class="supn">Noa Ben-David</div></div>
            <div class="supmsg">Message</div>
          </div>
          <div class="seclbl">Your Team · Waiters · Tel Aviv</div>
          <div style="background:#fff">
            <div class="crow"><div class="cav-c" style="background:linear-gradient(135deg,#9C7BD6,#5E3FA8)">TK</div><div class="ci"><div class="cn">Tomer Katz</div><div class="cp">Peer · same team & location</div></div></div>
            <div class="crow"><div class="cav-c" style="background:linear-gradient(135deg,#F472B6,#BE185D)">DR</div><div class="ci"><div class="cn">Dana Rosen</div><div class="cp">Peer · same team & location</div></div></div>
          </div>
          <div class="seclbl">Other Teams · Tel Aviv</div>
          <div style="background:#fff">
            <div class="crow"><div class="cav-c" style="background:linear-gradient(135deg,#FF6B6B,#C0392B)">MK</div><div class="ci"><div class="cn">Maya Koren</div><div class="cp">Kitchen · Tel Aviv</div></div></div>
            <div class="crow"><div class="cav-c" style="background:linear-gradient(135deg,#AB47BC,#6A1B9A)">BS</div><div class="ci"><div class="cn">Ben Shapira</div><div class="cp">Management · Tel Aviv</div></div></div>
          </div>
          <div class="seclbl">Other Locations</div>
          <div style="background:#fff">
            <div class="crow crow-dim" onclick="toggleRedirect(this)">
              <div class="cav-c" style="background:linear-gradient(135deg,#48C774,#2E7D32)">DL</div><div class="ci"><div class="cn">Dani Levi</div><div class="cp">Waiters · Herzliya</div></div>
            </div>
            <div class="redirect-note">📍 Different location — message Noa Ben-David and she'll connect you.</div>
            <div class="crow crow-dim" onclick="toggleRedirect(this)">
              <div class="cav-c" style="background:linear-gradient(135deg,#26C6DA,#00838F)">KH</div><div class="ci"><div class="cn">Kitchen Team</div><div class="cp">Kitchen · Herzliya</div></div>
            </div>
            <div class="redirect-note">📍 Different location — message Noa Ben-David and she'll connect you.</div>
          </div>
        </div>
        <div class="tabbar">
          <div class="tab"><div class="tab-iw"><svg><use href="#i-admin"/></svg></div><div class="tab-l">Admin</div></div>
          <div class="tab"><div class="tab-iw"><svg><use href="#i-ext"/></svg></div><div class="tab-l">Extensions</div></div>
          <div class="tab"><div class="tab-iw"><svg><use href="#i-lib"/></svg></div><div class="tab-l">Library</div></div>
          <div class="tab active"><div class="tab-iw"><svg><use href="#i-contacts"/></svg></div><div class="tab-l">Contacts</div></div>
          <div class="tab"><div class="tab-iw"><svg><use href="#i-home"/></svg></div><div class="tab-l">Home</div></div>
        </div>
      </div>
    </div>

    <!-- RIGHT: Cross-Team restricted (admin toggled on) -->
    <div class="variant-wrap">
      <div class="variant-lbl" style="color:#888">Cross-Team: restricted (admin toggled on)</div>
      <div class="phone full">
        <div class="sb"><span class="sb-t">10:45</span><div class="sb-r">●●● 🔋</div></div>
        <div class="nb"><div class="nb-back" onclick="prevPage()"><svg><use href="#i-chevl"/></svg></div><div class="nb-title">Contacts</div><div class="nb-sp"></div></div>
        <div style="background:#F8F8F8;padding-bottom:8px">
          <div class="nudge blue">
            <div class="nudge-x" onclick="this.closest('.nudge').remove()">✕</div>
            <span class="nudge-icon">✨</span>
            <div class="nudge-title">What's new: Teams & Locations</div>
            <div class="nudge-body">Your workspace is now organized by team and location. For questions outside your team, message your supervisor — they'll get you to the right person.</div>
          </div>
          <div class="suprow">
            <div class="supav" style="background:linear-gradient(135deg,#26C6DA,#00838F)">NB</div>
            <div class="supi"><div class="supl">Your supervisor</div><div class="supn">Noa Ben-David</div></div>
            <div class="supmsg">Message</div>
          </div>
          <div class="seclbl">Your Team · Waiters · Tel Aviv</div>
          <div style="background:#fff">
            <div class="crow"><div class="cav-c" style="background:linear-gradient(135deg,#9C7BD6,#5E3FA8)">TK</div><div class="ci"><div class="cn">Tomer Katz</div><div class="cp">Peer · same team & location</div></div></div>
            <div class="crow"><div class="cav-c" style="background:linear-gradient(135deg,#F472B6,#BE185D)">DR</div><div class="ci"><div class="cn">Dana Rosen</div><div class="cp">Peer · same team & location</div></div></div>
          </div>
          <div class="seclbl">Other Teams · Tel Aviv</div>
          <div style="background:#fff">
            <div class="crow crow-dim" onclick="toggleRedirect9(this)">
              <div class="cav-c" style="background:linear-gradient(135deg,#FF6B6B,#C0392B)">MK</div><div class="ci"><div class="cn">Maya Koren</div><div class="cp">Kitchen · Tel Aviv</div></div>
            </div>
            <div class="redirect-note">💬 Different team — message Noa Ben-David and she'll connect you.</div>
            <div class="crow crow-dim" onclick="toggleRedirect9(this)">
              <div class="cav-c" style="background:linear-gradient(135deg,#AB47BC,#6A1B9A)">BS</div><div class="ci"><div class="cn">Ben Shapira</div><div class="cp">Management · Tel Aviv</div></div>
            </div>
            <div class="redirect-note">💬 Different team — message Noa Ben-David and she'll connect you.</div>
          </div>
          <div class="seclbl">Other Locations</div>
          <div style="background:#fff">
            <div class="crow crow-dim" onclick="toggleRedirect9(this)">
              <div class="cav-c" style="background:linear-gradient(135deg,#48C774,#2E7D32)">DL</div><div class="ci"><div class="cn">Dani Levi</div><div class="cp">Waiters · Herzliya</div></div>
            </div>
            <div class="redirect-note">📍 Different location — message Noa Ben-David and she'll connect you.</div>
            <div class="crow crow-dim" onclick="toggleRedirect9(this)">
              <div class="cav-c" style="background:linear-gradient(135deg,#26C6DA,#00838F)">KH</div><div class="ci"><div class="cn">Kitchen Team</div><div class="cp">Kitchen · Herzliya</div></div>
            </div>
            <div class="redirect-note">📍 Different location — message Noa Ben-David and she'll connect you.</div>
          </div>
        </div>
        <div class="tabbar">
          <div class="tab"><div class="tab-iw"><svg><use href="#i-admin"/></svg></div><div class="tab-l">Admin</div></div>
          <div class="tab"><div class="tab-iw"><svg><use href="#i-ext"/></svg></div><div class="tab-l">Extensions</div></div>
          <div class="tab"><div class="tab-iw"><svg><use href="#i-lib"/></svg></div><div class="tab-l">Library</div></div>
          <div class="tab active"><div class="tab-iw"><svg><use href="#i-contacts"/></svg></div><div class="tab-l">Contacts</div></div>
          <div class="tab"><div class="tab-iw"><svg><use href="#i-home"/></svg></div><div class="tab-l">Home</div></div>
        </div>
      </div>
    </div>

  </div>
  <div class="ann"><div class="ann-dot"></div><div class="ann-txt"><strong>Same screen structure, two different admin decisions.</strong> <strong>Left (default):</strong> Cross-Team unrestricted — "Other Teams · Tel Aviv" is fully accessible, other locations dimmed. Waiter can reach Kitchen and Management at her location directly. <strong>Right:</strong> Cross-Team restricted — other teams at the same location are now dimmed too. The supervisor-routing pattern is identical in both cases: tap a dimmed contact, get a gentle nudge toward Noa rather than a dead end. The employee experience doesn't feel like a locked door — it feels like a phone book that tells you who to call. <strong>Contacts section stays visible regardless</strong>: hiding contacts entirely would feel more "policed" than dimming them. <strong>"What's new"</strong> banner updates its language per setting. <span style="color:#4A6CF7;font-weight:700">End of walkthrough — use Back to revisit any screen.</span></div></div>
</div>

<script>
const TOTAL = 10; // page 0 (cover) + Screens 1-9
let cur = 0;

function updateNav(){
  document.getElementById('backBtn').disabled = (cur === 0);
  document.getElementById('fwdBtn').disabled = (cur === TOTAL - 1);
  document.getElementById('pageIndicator').textContent = (cur === 0) ? 'Cover' : ('Screen ' + cur + ' of 9');
}
function goTo(n){
  if(n < 0 || n >= TOTAL) return;
  document.querySelectorAll('.page').forEach(function(p){
    p.classList.toggle('active', parseInt(p.dataset.page,10) === n);
  });
  cur = n;
  updateNav();
  window.scrollTo(0,0);
}
function nextPage(){ goTo(cur+1); }
function prevPage(){ goTo(cur-1); }

document.addEventListener('keydown', function(e){
  if(e.key === 'ArrowRight') nextPage();
  if(e.key === 'ArrowLeft') prevPage();
});

// ───────────────────────── Page 2: Locations ─────────────────────────
function toggleLoc(tog){
  const wrap = tog.closest('.loc-toggle-wrap');
  const off = wrap.querySelector('.loc-off-content');
  const on = wrap.querySelector('.loc-on-content');
  const sub = wrap.querySelector('.loc-sub');
  const isOn = tog.classList.contains('on');
  tog.classList.toggle('on', !isOn);
  tog.classList.toggle('off', isOn);
  off.style.display = isOn ? '' : 'none';
  on.style.display = isOn ? 'none' : '';
  sub.textContent = isOn
    ? 'Single site — you can switch this on anytime in Settings.'
    : 'Add each physical site your staff work from.';
}
function addLocation(){
  const list = document.getElementById('locList');
  const row = document.createElement('div');
  row.className = 'loc-input-row';
  row.innerHTML = '<div class="loc-dot"></div><input class="loc-input" placeholder="New location"><div class="loc-del" onclick="this.closest(\'.loc-input-row\').remove()">✕</div>';
  list.appendChild(row);
  row.querySelector('input').focus();
}

// ───────────────────────── Page 3: Industry & teams ─────────────────────────
const TEAM_CHIPS = {
  Restaurant: [['👨‍🍳','Kitchen','location'],['🍷','Waiters','location'],['💼','Management','all'],['🧹','Cleaning','location']],
  Hotel: [['🛎️','Front Desk','location'],['🧹','Housekeeping','location'],['👨‍🍳','Kitchen','location'],['💼','Management','all']],
  Retail: [['🛍️','Sales Floor','location'],['📦','Stockroom','location'],['💳','Checkout','location'],['💼','Management','all']],
  Healthcare: [['🩺','Nursing','location'],['🧪','Lab','location'],['📋','Reception','location'],['💼','Administration','all']],
  Construction: [['👷','Site Crew','location'],['🏗️','Foremen','location'],['📐','Engineering','all'],['💼','Management','all']],
  Other: []
};
function selectIndustry(card){
  document.querySelectorAll('.page[data-page="3"] .icard').forEach(function(c){ c.classList.remove('sel'); });
  card.classList.add('sel');
  renderChips(card.dataset.industry);
}
function renderChips(industry){
  const wrap = document.getElementById('teamChips');
  const addBtn = wrap.querySelector('.chip-add');
  wrap.querySelectorAll('.chip, .chip-empty').forEach(function(c){ c.remove(); });
  const list = TEAM_CHIPS[industry] || [];
  if(list.length === 0){
    const empty = document.createElement('div');
    empty.className = 'chip-empty';
    empty.textContent = 'Define your own teams below.';
    wrap.insertBefore(empty, addBtn);
    return;
  }
  list.forEach(function(item){
    const chip = document.createElement('div');
    chip.className = 'chip';
    chip.innerHTML = item[0] + ' ' + item[1] + ' <span class="chip-scope">· ' + item[2] + '</span><span class="chip-x">✕</span>';
    wrap.insertBefore(chip, addBtn);
  });
}

// ───────────────────────── Page 4: Org structure tier engine ─────────────────────────
let customTiers = [
  {id: 't1', name: 'Owner / GM', editing: false},
  {id: 't2', name: 'Shift Lead', editing: false},
  {id: 't3', name: 'Staff', editing: false}
];
let nextTierId = 4;
let prevHints = {};

const TIER_COLORS = ['#2E75B6', '#4A86C8', '#7AA8C8', '#A9C4DC'];
const TIER_LAST_COLOR = '#D5E8F0';

function computeHint(idx, arr){
  if(idx === 0) return 'Sees all branches · can message anyone';
  if(idx === arr.length - 1) return 'Sees their team only';
  const above = arr[idx-1].name && arr[idx-1].name.trim() ? arr[idx-1].name.trim() : 'the tier above';
  return 'Sees their team · can reach ' + above;
}

function renderTiers(){
  const container = document.getElementById('tierRows');
  let html = '';
  // Org Admin — locked, always first
  html += '<div class="tier-row">' +
    '<div class="tier-handle" style="visibility:hidden">⠿</div>' +
    '<div class="tier-num" style="background:#1F4E79;font-size:8px;margin-top:9px">★</div>' +
    '<div class="tier-pill-wrap">' +
      '<div class="tier-pill locked"><span class="tier-name locked">Org Admin</span><span style="font-size:10px;color:#7AA8C8;font-weight:600">System · 🔒</span></div>' +
      '<div class="tier-hint locked">Sees and manages everything</div>' +
    '</div></div>';

  customTiers.forEach(function(tier, idx){
    const num = idx + 1;
    const isLast = (idx === customTiers.length - 1);
    const hintText = computeHint(idx, customTiers);
    const changed = (prevHints[tier.id] !== undefined && prevHints[tier.id] !== hintText);
    const hintCls = 'tier-hint' + (changed ? ' updated' : '');
    const color = isLast ? TIER_LAST_COLOR : (TIER_COLORS[idx] || '#4A86C8');
    const numStyle = 'background:' + color + (isLast ? ';color:#2E75B6' : '') + ';margin-top:9px';

    if(tier.editing){
      html += '<div class="tier-row" data-id="' + tier.id + '">' +
        '<div class="tier-handle" style="visibility:hidden">⠿</div>' +
        '<div class="tier-num" style="' + numStyle + '">' + num + '</div>' +
        '<div class="tier-pill-wrap">' +
          '<div class="tier-pill editing">' +
            '<input id="input-' + tier.id + '" placeholder="Name this tier…" value="' + tier.name.replace(/"/g,'&quot;') + '" style="font-size:13px;font-weight:600;color:#000;border:none;background:transparent;width:120px;outline:none;font-family:inherit">' +
            '<span class="tier-actions"><span class="tier-edit" onclick="saveTier(\'' + tier.id + '\')">✓ Save</span></span>' +
          '</div>' +
          '<div class="' + hintCls + '">' + hintText + '</div>' +
        '</div></div>';
    } else {
      const delCls = 'tier-del' + (isLast ? ' off' : '');
      const delAttr = isLast ? '' : ' onclick="removeTier(\'' + tier.id + '\')"';
      html += '<div class="tier-row" draggable="true" data-id="' + tier.id + '" ' +
        'ondragstart="dragStart(event)" ondragover="dragOver(event)" ondragleave="dragLeave(event)" ondrop="dragDrop(event)" ondragend="dragEnd(event)">' +
        '<div class="tier-handle">⠿</div>' +
        '<div class="tier-num" style="' + numStyle + '">' + num + '</div>' +
        '<div class="tier-pill-wrap">' +
          '<div class="tier-pill">' +
            '<span class="tier-name">' + tier.name + '</span>' +
            '<span class="tier-actions"><span class="tier-edit" onclick="renameTier(\'' + tier.id + '\')">Rename</span><span class="' + delCls + '"' + delAttr + '>✕</span></span>' +
          '</div>' +
          '<div class="' + hintCls + '">' + hintText + '</div>' +
        '</div></div>';
    }
    prevHints[tier.id] = hintText;
  });

  container.innerHTML = html;
  updateExceptionLabels();
  renderTierSummary();
}

function renderTierSummary(){
  const summaryEl = document.getElementById('tierSummary');
  if(!summaryEl) return;
  const COLORS = ['#2E75B6','#4A86C8','#7AA8C8','#A9C4DC'];
  const LAST = '#D5E8F0';
  let html = '';
  // Org Admin row
  html += '<div class="tier-sum-row"><div class="tier-sum-num" style="background:#1F4E79;font-size:8px">★</div><div class="tier-sum-info"><div class="tier-sum-name">Org Admin</div><div class="tier-sum-hint">Sees and manages everything</div></div></div>';
  customTiers.forEach(function(t,i){
    const isLast = i === customTiers.length - 1;
    const color = isLast ? LAST : (COLORS[i] || '#4A86C8');
    const numStyle = 'background:' + color + (isLast ? ';color:#2E75B6' : '');
    const hint = computeHint(i, customTiers);
    html += '<div class="tier-sum-row"><div class="tier-sum-num" style="' + numStyle + '">' + (i+1) + '</div><div class="tier-sum-info"><div class="tier-sum-name">' + (t.name || 'Unnamed') + '</div><div class="tier-sum-hint">' + hint + '</div></div></div>';
  });
  summaryEl.innerHTML = html;
}

function toggleCustomize(el){
  const editor = document.getElementById('custEditor');
  const isOpen = editor.classList.contains('open');
  editor.classList.toggle('open', !isOpen);
  el.textContent = isOpen ? '▾ Customize hierarchy' : '▴ Collapse';
}

function toggleBulkSection(el){
  const section = document.getElementById('bulkSection');
  const isOpen = section.classList.contains('open');
  section.classList.toggle('open', !isOpen);
  el.textContent = isOpen ? '▾ Bulk actions' : '▴ Bulk actions';
}

function switchAssignState(state){
  const populated = document.getElementById('assignPopulatedState');
  const empty = document.getElementById('assignEmptyState');
  const tabP = document.getElementById('tab-populated');
  const tabE = document.getElementById('tab-empty');
  if(state === 'empty'){
    populated.style.display = 'none';
    empty.style.display = '';
    tabP.style.background = '#F0F0F0'; tabP.style.color = '#888';
    tabE.style.background = '#4A6CF7'; tabE.style.color = '#fff';
  } else {
    populated.style.display = '';
    empty.style.display = 'none';
    tabP.style.background = '#4A6CF7'; tabP.style.color = '#fff';
    tabE.style.background = '#F0F0F0'; tabE.style.color = '#888';
  }
}

function toggleBoundary(tog, kind){
  const isOn = tog.classList.contains('on');
  tog.classList.toggle('on', !isOn);
  tog.classList.toggle('off', isOn);
  const restricted = !isOn; // toggle now ON means the restriction is active
  if(kind === 'team'){
    document.getElementById('teamOpenList').style.display = restricted ? 'none' : '';
    document.getElementById('teamRestrictList').style.display = restricted ? '' : 'none';
    document.getElementById('teamException').style.display = restricted ? '' : 'none';
  } else {
    document.getElementById('locRestrictList').style.display = restricted ? '' : 'none';
    document.getElementById('locOpenList').style.display = restricted ? 'none' : '';
    document.getElementById('locException').style.display = restricted ? '' : 'none';
  }
}
function selectException(el){
  const group = el.closest('.bound-exception');
  group.querySelectorAll('.bound-radio').forEach(function(r){ r.classList.remove('sel'); });
  el.classList.add('sel');
}
function updateExceptionLabels(){
  const label = (customTiers.length >= 2 && customTiers[1].name && customTiers[1].name.trim())
    ? customTiers[1].name.trim() + ' and above'
    : 'second-from-top tier and above';
  document.querySelectorAll('.exc-label-1').forEach(function(el){ el.textContent = label; });
}

function addTier(){
  customTiers.splice(1, 0, {id: 't' + (nextTierId++), name: '', editing: true});
  renderTiers();
  const input = document.querySelector('.tier-pill.editing input');
  if(input) input.focus();
}
function removeTier(id){
  if(customTiers.length <= 1) return;
  customTiers = customTiers.filter(function(t){ return t.id !== id; });
  delete prevHints[id];
  renderTiers();
}
function renameTier(id){
  customTiers.forEach(function(t){ if(t.id === id) t.editing = true; });
  renderTiers();
  const input = document.getElementById('input-' + id);
  if(input) input.focus();
}
function saveTier(id){
  const input = document.getElementById('input-' + id);
  const val = input ? input.value.trim() : '';
  customTiers.forEach(function(t){
    if(t.id === id){ t.name = val || 'Untitled'; t.editing = false; }
  });
  renderTiers();
}

// drag and drop reordering
let dragSrcId = null;
function dragStart(e){
  dragSrcId = e.currentTarget.dataset.id;
  e.dataTransfer.effectAllowed = 'move';
}
function dragOver(e){
  e.preventDefault();
  e.currentTarget.classList.add('drag-over');
}
function dragLeave(e){
  e.currentTarget.classList.remove('drag-over');
}
function dragDrop(e){
  e.preventDefault();
  e.currentTarget.classList.remove('drag-over');
  const targetId = e.currentTarget.dataset.id;
  if(!dragSrcId || targetId === dragSrcId) return;
  const srcIdx = customTiers.findIndex(function(t){ return t.id === dragSrcId; });
  const tgtIdx = customTiers.findIndex(function(t){ return t.id === targetId; });
  if(srcIdx === -1 || tgtIdx === -1) return;
  const moved = customTiers.splice(srcIdx, 1)[0];
  customTiers.splice(tgtIdx, 0, moved);
  renderTiers();
}
function dragEnd(e){
  document.querySelectorAll('.tier-row.drag-over').forEach(function(r){ r.classList.remove('drag-over'); });
  dragSrcId = null;
}

// ───────────────────────── Page 5: Assign members ─────────────────────────
const TEAM_OPTIONS = ['Kitchen','Waiters','Mgmt','Cleaning'];
const LOC_OPTIONS = ['TLV','HRZ'];
const memberData = {
  yoav: {teams:['Mgmt'], locs:['TLV']},
  maya: {teams:['Kitchen'], locs:['TLV']},
  dani: {teams:['Waiters'], locs:['HRZ']},
  rina: {teams:[], locs:[]},
  ben:  {teams:['Mgmt','Waiters'], locs:['TLV','HRZ']},
  noa:  {teams:['Waiters'], locs:['TLV']}
};
function pillHTML(id, kind, arr, updated){
  const opts = (kind === 'teams') ? TEAM_OPTIONS : LOC_OPTIONS;
  const grCls = (kind === 'locs') ? ' gr' : '';
  const updCls = updated ? ' updated' : '';
  if(arr.length === 0){
    const placeholder = (kind === 'teams') ? 'Team ▾' : 'Loc ▾';
    let opt = '<option value="" selected disabled hidden>' + placeholder + '</option>';
    opts.forEach(function(o){ opt += '<option value="' + o + '">' + o + '</option>'; });
    return '<select class="bdd-select un' + updCls + '" onchange="setSingle(\'' + id + '\',\'' + kind + '\',this.value)">' + opt + '</select>';
  }
  if(arr.length === 1){
    let opt = '';
    opts.forEach(function(o){ opt += '<option value="' + o + '"' + (o === arr[0] ? ' selected' : '') + '>' + o + '</option>'; });
    return '<select class="bdd-select' + grCls + updCls + '" onchange="setSingle(\'' + id + '\',\'' + kind + '\',this.value)">' + opt + '</select>';
  }
  const label = arr.length + ' ' + (kind === 'teams' ? 'teams' : 'locs') + ' ▾';
  return '<span class="bdd' + grCls + updCls + '" style="font-size:10px">' + label + '</span>';
}
function renderPills(id, markUpdated){
  ['pills-', 'bulk-pills-'].forEach(function(prefix){
    const el = document.getElementById(prefix + id);
    if(!el) return;
    const m = memberData[id];
    el.innerHTML = pillHTML(id,'teams',m.teams,markUpdated) + pillHTML(id,'locs',m.locs,markUpdated);
  });
}
function setSingle(id, kind, val){
  memberData[id][kind] = [val];
  renderPills(id);
}
function toggleChk(el){
  el.classList.toggle('on');
  el.textContent = el.classList.contains('on') ? '✓' : '';
  const checked = document.querySelectorAll('#bulkSection .bchk.on').length;
  const bar = document.getElementById('bulkBar');
  if(checked >= 2){
    document.getElementById('bulkCount').textContent = checked + ' selected';
    bar.style.display = 'flex';
  } else {
    bar.style.display = 'none';
  }
}
function bulkClear(){
  document.querySelectorAll('#bulkSection .bchk.on').forEach(function(c){
    c.classList.remove('on');
    c.textContent = '';
  });
  document.getElementById('bulkBar').style.display = 'none';
}
function bulkApply(){
  const team = document.getElementById('bulkTeam').value;
  const loc = document.getElementById('bulkLoc').value;
  document.querySelectorAll('#bulkSection .bchk.on').forEach(function(chk){
    const id = chk.dataset.member;
    const m = memberData[id];
    if(m.teams.indexOf(team) === -1) m.teams.push(team);
    if(m.locs.indexOf(loc) === -1) m.locs.push(loc);
    renderPills(id, true);
  });
  bulkClear();
}

// ───────────────────────── Page 6: Activate toast ─────────────────────────
function activate(){
  const toast = document.getElementById('toast');
  toast.classList.add('show');
  setTimeout(function(){
    toast.classList.remove('show');
    nextPage();
  }, 1400);
}

// ───────────────────────── Page 7: My Company ─────────────────────────
function openSort(){
  document.getElementById('sortOverlay').classList.add('show');
}
function selectSort(opt){
  document.querySelectorAll('#sortOpts .sort-opt').forEach(function(o){ o.classList.remove('sel'); });
  opt.classList.add('sel');
}
function applySort(){
  const sel = document.querySelector('#sortOpts .sort-opt.sel');
  const label = sel ? sel.textContent.replace('✓','').trim() : 'Unassigned first';
  document.getElementById('sortLabel').textContent = label + ' ▾';
  document.getElementById('sortOverlay').classList.remove('show');
}
function assignRina(){
  document.getElementById('rinaStatus').outerHTML = '<div class="bdds" style="margin-top:1px"><div class="bdd">Waiters ▾</div><div class="bdd gr">TLV ▾</div></div>';
  document.getElementById('rinaAssignBtn').remove();
  document.getElementById('unassignedCount').textContent = '⚠️ 1 member not yet assigned';
}

// ───────────────────────── Page 9: Contacts ─────────────────────────
function toggleRedirect(row){
  const note = row.nextElementSibling;
  if(note && note.classList.contains('redirect-note')) note.classList.toggle('show');
}
function toggleRedirect9(row){
  const note = row.nextElementSibling;
  if(note && note.classList.contains('redirect-note')) note.classList.toggle('show');
}

// ───────────────────────── init ─────────────────────────
renderTiers();
renderTierSummary();
Object.keys(memberData).forEach(function(id){ renderPills(id); });
updateNav();
</script>
</body>
</html>
