---
title: "May 12, 2017: OpenModelica 1.12.0-dev.alpha1 released"
---
<p>&nbsp;The OpenModelica 1.12.0-dev.alpha1 has been released. You can find the Windows builds&nbsp;<a href="download/download-windows" target="_blank">here</a>. The Linux and MacOS builds are available via the Download menu above.</p>
<p><strong style="color: #222222; line-height: 1.2;"><span style="font-size: 14pt;">OpenModelica 1.12.0-dev.alpha1 release, May 12, 2017</span></strong></p>
<p>Summary of most important improvements:</p>
<p class="Appendix3"><span style="font-size: 12pt;"><strong>OpenModelica Compiler (OMC)</strong></span></p>
<ul>
<li style="line-height: 17.6px;">Initializing external objects together with parameters</li>
<li style="line-height: 17.6px;">Handle exceptions in numeric solvers</li>
<li style="line-height: 17.6px;">Support for higher-index discrete clock partitions</li>
<li style="line-height: 17.6px;">Improved unit checking</li>
<li style="line-height: 17.6px;">Improved initialization of start values</li>
<li style="line-height: 17.6px;">New approach for homotopy-based &nbsp;initialization (still experimental)</li>
<li style="line-height: 17.6px;">A bunch of fixes: Bugs, regressions, performance issues</li>
<li style="line-height: 17.6px;">Improved Dynamic Tearing by adding constraints for the casual set</li>
<li style="line-height: 17.6px;">Improved module wrapFunctionCalls with one-time evaluation of Constant CSE-variables</li>
<li style="line-height: 17.6px;">Added initOptModule for inlineHomotopy</li>
<li style="line-height: 17.6px;">Added configuration flag tearingStrictness to influence solvability</li>
<li style="line-height: 17.6px;">New methods for inline integration for continuous equations in clocked partitions, now covering: ExplicitEuler, ImplicitEuler, SemiImplicitEuler and ImplicitTrapezoid</li>
<li style="line-height: 17.6px;">Complete implementation of synchronous features in Cpp runtime</li>
<li style="line-height: 17.6px;">Refactored linear solver of Cpp runtime</li>
<li style="line-height: 17.6px;">Improved Modelica_Synchronous_Cpp coverage</li>
<li style="line-height: 17.6px;">Coverage of most of the OpenHydraulics library</li>
<li style="line-height: 17.6px;">Support for Modelica Device Drivers library</li>
<li style="line-height: 17.6px;">Support of time events for cpp-simulation and enabled time events in cpp-FMUs</li>
</ul>
<p class="Appendix3"><strong style="font-size: 12pt;">Graphic Editor OMEdit</strong></p>
<ul>
<li style="line-height: 17.6px;">Additional advanced visualization features for multibody animation (transparency, textures, change colours by dialog)</li>
<li style="line-height: 17.6px;">An HTML WYSIWYG Editor, e.g. useful for documentation</li>
<li style="line-height: 17.6px;">Support for choices(checkBox=true) annotation.</li>
<li style="line-height: 17.6px;">Support for loadSelector &amp; saveSelector attribute of Dialog annotation.</li>
<li style="line-height: 17.6px;">Panning of icon/diagram view and plot window.</li>
<li style="line-height: 17.6px;">AutoComplete feature in text editing for keywords, types, common Modelica constructs</li>
<li style="line-height: 17.6px;">Follow connector transformation from Diagram View to Icon View.</li>
<li style="line-height: 17.6px;">Replaceable GUI support essentially completed, will be in the final 1.12.0 release but not yet in the alpha release due to performance problems in the old frontend.</li>
<li style="line-height: 17.6px;">Further stability improvements</li>
<li style="line-height: 17.6px;">Improved performance for rendering some icons using the interactive API</li>
<li style="line-height: 17.6px;">Improved handling of parameters that cannot be evaluated in Icon annotations</li>
</ul>
<p><strong style="font-size: 12pt;">FMI Support</strong></p>
<ul>
<li>A new (stand-alone) FMI- and TLM-based simulation tool OMSimulator, first version (a main deliverable of the OPENCPS project, significant contributions and code donations from SKF)</li>
<li>Graphic configuration editing of composite models consisting of FMUs</li>
<li>Co-simulation/simulation of connected FMUs, TLM objects, Simulink models (via wrappers), Adams models (via wrappers), BEAST models (via wrappers), Modelica models.</li>
<li>Updated implementation for synchronous models according to current FCP001 (FMI Change Proposal), with better treatment of states, more flexibility in evaluation of FMUs, useful for optimization using FMUs, and approximate Jacobians.</li>
</ul>
<p><strong style="font-size: 12pt;">Other things</strong></p>
<ul>
<li style="line-height: 17.6px;">Modelica-based requirement modeling in OpenModelica. Requirements can be expressed using Martin Otters Requirement library, standard Modelica, any other libraries, state machines</li>
<li style="line-height: 17.6px;">Textual support through OpenModelica API and graphical support in OMEdit for generation of single or multiple requirement verification scenarios</li>
<li style="line-height: 17.6px;">VVDRlib – a small library for connecting requirements and models together, with notions for mediators, scenarios, design alternatives</li>
<li style="line-height: 17.6px;">Further enhanced OMPython including linearization</li>
<li style="line-height: 17.6px;">New enhanced library testing script (libraries.openmodelica.org/branches).</li>
<li style="line-height: 17.6px;">Addition of mutable reference data types in MetaModelica</li>
<li style="line-height: 17.6px;">Support for RedHat/Fedora binary builds of OpenModelica</li>
</ul>
<div id="_mcePaste" class="mcePaste" data-mce-bogus="1" style="position: absolute; left: 0px; top: -25px; width: 1px; height: 1px; overflow: hidden;">
<p class="BulletItem" style="margin-left: .5in; text-indent: -.25in; line-height: 13.0pt; mso-line-height-rule: exactly; mso-list: l0 level1 lfo2; tab-stops: list .5in;"><!--[if !supportLists]--><span lang="EN-US" style="font-size: 10.0pt; mso-bidi-font-size: 12.0pt; font-family: Symbol; mso-fareast-font-family: Symbol; mso-bidi-font-family: Symbol;">·<span style="font-variant-numeric: normal; font-stretch: normal; font-size: 7pt; line-height: normal; font-family: 'Times New Roman';">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span><!--[endif]--><span lang="EN-US">Initializing external objects together with parameters<o:p></o:p></span></p>
<p class="BulletItem" style="margin-left: .5in; text-indent: -.25in; line-height: 13.0pt; mso-line-height-rule: exactly; mso-list: l0 level1 lfo2; tab-stops: list .5in;"><!--[if !supportLists]--><span lang="EN-US" style="font-size: 10.0pt; mso-bidi-font-size: 12.0pt; font-family: Symbol; mso-fareast-font-family: Symbol; mso-bidi-font-family: Symbol;">·<span style="font-variant-numeric: normal; font-stretch: normal; font-size: 7pt; line-height: normal; font-family: 'Times New Roman';">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span><!--[endif]--><span lang="EN-US">Handle exceptions in numeric solvers<o:p></o:p></span></p>
<p class="BulletItem" style="margin-left: .5in; text-indent: -.25in; line-height: 13.0pt; mso-line-height-rule: exactly; mso-list: l0 level1 lfo2; tab-stops: list .5in;"><!--[if !supportLists]--><span lang="EN-US" style="font-size: 10.0pt; mso-bidi-font-size: 12.0pt; font-family: Symbol; mso-fareast-font-family: Symbol; mso-bidi-font-family: Symbol;">·<span style="font-variant-numeric: normal; font-stretch: normal; font-size: 7pt; line-height: normal; font-family: 'Times New Roman';">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span><!--[endif]--><span lang="EN-US">Support for higher-index discrete clock partitions<o:p></o:p></span></p>
<p class="BulletItem" style="margin-left: .5in; text-indent: -.25in; line-height: 13.0pt; mso-line-height-rule: exactly; mso-list: l0 level1 lfo2; tab-stops: list .5in;"><!--[if !supportLists]--><span lang="EN-US" style="font-size: 10.0pt; mso-bidi-font-size: 12.0pt; font-family: Symbol; mso-fareast-font-family: Symbol; mso-bidi-font-family: Symbol;">·<span style="font-variant-numeric: normal; font-stretch: normal; font-size: 7pt; line-height: normal; font-family: 'Times New Roman';">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span><!--[endif]--><span lang="EN-US">Improved unit checking<o:p></o:p></span></p>
<p class="BulletItem" style="margin-left: .5in; text-indent: -.25in; line-height: 13.0pt; mso-line-height-rule: exactly; mso-list: l0 level1 lfo2; tab-stops: list .5in;"><!--[if !supportLists]--><span lang="EN-US" style="font-size: 10.0pt; mso-bidi-font-size: 12.0pt; font-family: Symbol; mso-fareast-font-family: Symbol; mso-bidi-font-family: Symbol;">·<span style="font-variant-numeric: normal; font-stretch: normal; font-size: 7pt; line-height: normal; font-family: 'Times New Roman';">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span><!--[endif]--><span lang="EN-US">Improved initialization of start values<o:p></o:p></span></p>
<p class="BulletItem" style="margin-left: .5in; text-indent: -.25in; line-height: 13.0pt; mso-line-height-rule: exactly; mso-list: l0 level1 lfo2; tab-stops: list .5in;"><!--[if !supportLists]--><span lang="EN-US" style="font-size: 10.0pt; mso-bidi-font-size: 12.0pt; font-family: Symbol; mso-fareast-font-family: Symbol; mso-bidi-font-family: Symbol;">·<span style="font-variant-numeric: normal; font-stretch: normal; font-size: 7pt; line-height: normal; font-family: 'Times New Roman';">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span><!--[endif]--><span lang="EN-US">New approach for homotopy-based&nbsp; initialization (still experimental)<o:p></o:p></span></p>
<p class="BulletItem" style="margin-left: .5in; text-indent: -.25in; line-height: 13.0pt; mso-line-height-rule: exactly; mso-list: l0 level1 lfo2; tab-stops: list .5in;"><!--[if !supportLists]--><span lang="EN-US" style="font-size: 10.0pt; mso-bidi-font-size: 12.0pt; font-family: Symbol; mso-fareast-font-family: Symbol; mso-bidi-font-family: Symbol;">·<span style="font-variant-numeric: normal; font-stretch: normal; font-size: 7pt; line-height: normal; font-family: 'Times New Roman';">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span><!--[endif]--><span lang="EN-US">A bunch of fixes: Bugs, regressions, performance issues<o:p></o:p></span></p>
<p class="BulletItem" style="margin-left: .5in; text-indent: -.25in; line-height: 13.0pt; mso-line-height-rule: exactly; mso-list: l0 level1 lfo2; tab-stops: list .5in;"><!--[if !supportLists]--><span lang="EN-US" style="font-size: 10.0pt; mso-bidi-font-size: 12.0pt; font-family: Symbol; mso-fareast-font-family: Symbol; mso-bidi-font-family: Symbol;">·<span style="font-variant-numeric: normal; font-stretch: normal; font-size: 7pt; line-height: normal; font-family: 'Times New Roman';">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span><!--[endif]--><span lang="EN-US">Improved Dynamic Tearing by adding constraints for the casual set<o:p></o:p></span></p>
<p class="BulletItem" style="margin-left: .5in; text-indent: -.25in; line-height: 13.0pt; mso-line-height-rule: exactly; mso-list: l0 level1 lfo2; tab-stops: list .5in;"><!--[if !supportLists]--><span lang="EN-US" style="font-size: 10.0pt; mso-bidi-font-size: 12.0pt; font-family: Symbol; mso-fareast-font-family: Symbol; mso-bidi-font-family: Symbol;">·<span style="font-variant-numeric: normal; font-stretch: normal; font-size: 7pt; line-height: normal; font-family: 'Times New Roman';">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span><!--[endif]--><span lang="EN-US">Improved module wrapFunctionCalls with one-time evaluation of Constant CSE-variables<o:p></o:p></span></p>
<p class="BulletItem" style="margin-left: .5in; text-indent: -.25in; line-height: 13.0pt; mso-line-height-rule: exactly; mso-list: l0 level1 lfo2; tab-stops: list .5in;"><!--[if !supportLists]--><span lang="EN-US" style="font-size: 10.0pt; mso-bidi-font-size: 12.0pt; font-family: Symbol; mso-fareast-font-family: Symbol; mso-bidi-font-family: Symbol;">·<span style="font-variant-numeric: normal; font-stretch: normal; font-size: 7pt; line-height: normal; font-family: 'Times New Roman';">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span><!--[endif]--><span lang="EN-US">Added initOptModule for inlineHomotopy<o:p></o:p></span></p>
<p class="BulletItem" style="margin-left: .5in; text-indent: -.25in; line-height: 13.0pt; mso-line-height-rule: exactly; mso-list: l0 level1 lfo2; tab-stops: list .5in;"><!--[if !supportLists]--><span lang="EN-US" style="font-size: 10.0pt; mso-bidi-font-size: 12.0pt; font-family: Symbol; mso-fareast-font-family: Symbol; mso-bidi-font-family: Symbol;">·<span style="font-variant-numeric: normal; font-stretch: normal; font-size: 7pt; line-height: normal; font-family: 'Times New Roman';">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span><!--[endif]--><span lang="EN-US">Added configuration flag tearingStrictness to influence solvability<o:p></o:p></span></p>
<p class="BulletItem" style="margin-left: .5in; text-indent: -.25in; line-height: 13.0pt; mso-line-height-rule: exactly; mso-list: l0 level1 lfo2; tab-stops: list .5in;"><!--[if !supportLists]--><span lang="EN-US" style="font-size: 10.0pt; mso-bidi-font-size: 12.0pt; font-family: Symbol; mso-fareast-font-family: Symbol; mso-bidi-font-family: Symbol;">·<span style="font-variant-numeric: normal; font-stretch: normal; font-size: 7pt; line-height: normal; font-family: 'Times New Roman';">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span><!--[endif]--><span lang="EN-US">New methods for inline integration for continuous equations in clocked partitions, now covering: ExplicitEuler, ImplicitEuler, SemiImplicitEuler and ImplicitTrapezoid<o:p></o:p></span></p>
<p class="BulletItem" style="margin-left: .5in; text-indent: -.25in; line-height: 13.0pt; mso-line-height-rule: exactly; mso-list: l0 level1 lfo2; tab-stops: list .5in;"><!--[if !supportLists]--><span lang="EN-US" style="font-size: 10.0pt; mso-bidi-font-size: 12.0pt; font-family: Symbol; mso-fareast-font-family: Symbol; mso-bidi-font-family: Symbol;">·<span style="font-variant-numeric: normal; font-stretch: normal; font-size: 7pt; line-height: normal; font-family: 'Times New Roman';">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span><!--[endif]--><span lang="EN-US">Complete implementation of synchronous features in Cpp runtime<o:p></o:p></span></p>
<p class="BulletItem" style="margin-left: .5in; text-indent: -.25in; line-height: 13.0pt; mso-line-height-rule: exactly; mso-list: l0 level1 lfo2; tab-stops: list .5in;"><!--[if !supportLists]--><span lang="EN-US" style="font-size: 10.0pt; mso-bidi-font-size: 12.0pt; font-family: Symbol; mso-fareast-font-family: Symbol; mso-bidi-font-family: Symbol;">·<span style="font-variant-numeric: normal; font-stretch: normal; font-size: 7pt; line-height: normal; font-family: 'Times New Roman';">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span><!--[endif]--><span lang="EN-US">Refactored linear solver of Cpp runtime<o:p></o:p></span></p>
<p class="BulletItem" style="margin-left: .5in; text-indent: -.25in; line-height: 13.0pt; mso-line-height-rule: exactly; mso-list: l0 level1 lfo2; tab-stops: list .5in;"><!--[if !supportLists]--><span lang="EN-US" style="font-size: 10.0pt; mso-bidi-font-size: 12.0pt; font-family: Symbol; mso-fareast-font-family: Symbol; mso-bidi-font-family: Symbol;">·<span style="font-variant-numeric: normal; font-stretch: normal; font-size: 7pt; line-height: normal; font-family: 'Times New Roman';">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span><!--[endif]--><span lang="EN-US">Improved Modelica_synchronous_cpp coverage<o:p></o:p></span></p>
<p class="BulletItem" style="margin-left: .5in; text-indent: -.25in; line-height: 13.0pt; mso-line-height-rule: exactly; mso-list: l0 level1 lfo2; tab-stops: list .5in;"><!--[if !supportLists]--><span lang="EN-US" style="font-size: 10.0pt; mso-bidi-font-size: 12.0pt; font-family: Symbol; mso-fareast-font-family: Symbol; mso-bidi-font-family: Symbol;">·<span style="font-variant-numeric: normal; font-stretch: normal; font-size: 7pt; line-height: normal; font-family: 'Times New Roman';">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span><!--[endif]--><span lang="EN-US">Coverage of most of the OpenHydraulics library<o:p></o:p></span></p>
<span lang="EN-GB" style="font-size: 11.0pt; mso-bidi-font-size: 12.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-ansi-language: EN-GB; mso-fareast-language: EN-US; mso-bidi-language: AR-SA;">Support of time events for cpp-simulation and enabled time events in cpp-FMUs</span></div>