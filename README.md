HEVC ENCODER AUTOMATED TEST
===================


This work has the objective is help researchers and developers in the test steps of HEVC encoder development process.
----------


How use this tool??
--------------------

In the directory "codec_test_tool", usu the *make* command for generate the executable program.
		
	$make

Run the binary program using the *./bin/EncoderTest* and the parameters of the test.

	./bin/EncoderTest -mod 1 -thr 2 -f 300 -fr 30 -eva encoderEva -ref encoderRef -vin 1 video.yuv -vout videosout/ -cfg 1 config.cfg -outl filelog/ -qp 4 22 27 32 37
	 
Command     | Description												| Default values
-------- 	| ---														| ---
-thr     	| Number of encoder instances running simultaneously* 		| 2
-eva     	| Encoder to be evaluated									| test/encoder/eva
-ref     	| Reference encoder 										| test/encoder/ref
-dec 	 	| Default decoder (use only to objective metrics) 			| test/decoder/dec
-vin     	| Number of videos followed by the input video sequences	| 1	test/vin/video.yuv
-outv     	| Output video path 										| test/vin/video.yuv
-outl     	| Output log file path										| test/vout/
-outl     	| Output log file path										| test/log/
-cfg     	| Number of cfg files followed by the cfg path files 		| 1 test/cfg/config.cfg
-f     		| Total frames used in test 								| 130
-fr     	| Frame rate 												| 30
-wdt     	| Video resolution width 									| 352
-hgt     	| Video resolution height 									| 288
-bdepth 	| Bit depth per color component 							| 8
-subsamp 	| Chroma subsampling 										| 4:2:0
-qp     	| Number of QP followed by the QPs 							| 4 22 27 32 37
-bd     	| Bjontegaard metric. 										| true
-ssim		| Structural Similarity Index metric.						| false
-pwssim 	| Perceptual Weighting Structural Similarity Index metric.	| false


\*Check the number of CPU cores in your computer!.
