 carrasco\_saccade html,body,div,span,applet,object,iframe,h1,h2,h3,h4,h5,h6,p,blockquote,pre,a,abbr,acronym,address,big,cite,code,del,dfn,em,font,img,ins,kbd,q,s,samp,small,strike,strong,sub,sup,tt,var,b,u,i,center,dl,dt,dd,ol,ul,li,fieldset,form,label,legend,table,caption,tbody,tfoot,thead,tr,th,td{margin:0;padding:0;border:0;outline:0;font-size:100%;vertical-align:baseline;background:transparent}body{line-height:1}ol,ul{list-style:none}blockquote,q{quotes:none}blockquote:before,blockquote:after,q:before,q:after{content:'';content:none}:focus{outine:0}ins{text-decoration:none}del{text-decoration:line-through}table{border-collapse:collapse;border-spacing:0} html { min-height:100%; margin-bottom:1px; } html body { height:100%; margin:0px; font-family:Arial, Helvetica, sans-serif; font-size:10px; color:#000; line-height:140%; background:#fff none; overflow-y:scroll; } html body td { vertical-align:top; text-align:left; } h1 { padding:0px; margin:0px 0px 25px; font-family:Arial, Helvetica, sans-serif; font-size:1.5em; color:#d55000; line-height:100%; font-weight:normal; } h2 { padding:0px; margin:0px 0px 8px; font-family:Arial, Helvetica, sans-serif; font-size:1.2em; color:#000; font-weight:bold; line-height:140%; border-bottom:1px solid #d6d4d4; display:block; } h3 { padding:0px; margin:0px 0px 5px; font-family:Arial, Helvetica, sans-serif; font-size:1.1em; color:#000; font-weight:bold; line-height:140%; } a { color:#005fce; text-decoration:none; } a:hover { color:#005fce; text-decoration:underline; } a:visited { color:#004aa0; text-decoration:none; } p { padding:0px; margin:0px 0px 20px; } img { padding:0px; margin:0px 0px 20px; border:none; } p img, pre img, tt img, li img, h1 img, h2 img { margin-bottom:0px; } ul { padding:0px; margin:0px 0px 20px 23px; list-style:square; } ul li { padding:0px; margin:0px 0px 7px 0px; } ul li ul { padding:5px 0px 0px; margin:0px 0px 7px 23px; } ul li ol li { list-style:decimal; } ol { padding:0px; margin:0px 0px 20px 0px; list-style:decimal; } ol li { padding:0px; margin:0px 0px 7px 23px; list-style-type:decimal; } ol li ol { padding:5px 0px 0px; margin:0px 0px 7px 0px; } ol li ol li { list-style-type:lower-alpha; } ol li ul { padding-top:7px; } ol li ul li { list-style:square; } .content { font-size:1.2em; line-height:140%; padding: 20px; } pre, code { font-size:12px; } tt { font-size: 1.2em; } pre { margin:0px 0px 20px; } pre.codeinput { padding:10px; border:1px solid #d3d3d3; background:#f7f7f7; } pre.codeoutput { padding:10px 11px; margin:0px 0px 20px; color:#4c4c4c; } pre.error { color:red; } @media print { pre.codeinput, pre.codeoutput { word-wrap:break-word; width:100%; } } span.keyword { color:#0000FF } span.comment { color:#228B22 } span.string { color:#A020F0 } span.untermstring { color:#B20000 } span.syscmd { color:#B28C00 } .footer { width:auto; padding:10px 0px; margin:25px 0px 0px; border-top:1px dotted #878787; font-size:0.8em; line-height:140%; font-style:italic; color:#878787; text-align:left; float:none; } .footer p { margin:0px; } .footer a { color:#878787; } .footer a:hover { color:#878787; text-decoration:underline; } .footer a:visited { color:#878787; } table th { padding:7px 5px; text-align:left; vertical-align:middle; border: 1px solid #d6d4d4; font-weight:bold; } table td { padding:7px 5px; text-align:left; vertical-align:top; border:1px solid #d6d4d4; }

Contents
--------

*   [\---- Carrasco Paradigm: Saccade ----](#1)
*   [TMS Initialization](#2)
*   [Get name, write file](#3)
*   [Screen Initialization](#4)
*   [Screen Parameters (taken from Iiyama HM204DT-A Manual)](#5)
*   [More params](#6)
*   [Eyelink Stuff](#7)
*   [Variable initialization](#8)
*   [Create all the gabors beforehand (faster!)](#9)
*   [Create Textures (allows for fast switch of screen)](#14)
*   [Draw fixation w/ left-pointing cue](#15)
*   [Draw boxes](#16)
*   [Draw fixation w/ right-pointing cue](#17)
*   [Draw boxes](#18)
*   [Experiment about to start](#19)
*   [Task](#20)
*   [Fixation](#22)
*   [Standard](#23)
*   [Draw fixation](#24)
*   [Fixation](#25)
*   [Cue](#26)
*   [Stimuli](#27)
*   [Draw fixation w/ left-pointing cue](#28)
*   [Draw gabor](#29)
*   [Draw fixation w/ right-pointing cue](#30)
*   [Draw gabor](#31)
*   [Draw boxes](#32)
*   [Ask which one](#33)
*   [Photodiode Stuff](#35)
*   [Write Excel](#36)
*   [Eyelink data](#37)

\---- Carrasco Paradigm: Saccade ----
-------------------------------------

Rolfs M, Carrasco C. “Rapid Simultaneous Enhancement of Visual Sensitivity and Perceived Contrast during Saccade Preparation.” J.Neurosci.(2012): 13744–13752.

Brainard, D. H. (1997) The Psychophysics Toolbox, Spatial Vision 10:433-436.

Pelli, D. G. (1997) The VideoToolbox software for visual psychophysics: Transforming numbers into movies, Spatial Vision 10:437-442.

Kleiner M, Brainard D, Pelli D, 2007, “What’s new in Psychtoolbox-3?” Perception 36 ECVP Abstract Supplement.

Software by Sacha McElligott ([sacha@nyu.edu](mailto:sacha@nyu.edu)) -- Last Update: July 31 2018 - with a few lines of code by: - Calin Manea - authors of "EyelinkExample.m" - Theresa Desrochers - Peter Scarfe

sca;
close all;
clc;
daqreset;
cd C:\\Users\\smcellig\\Desktop;
addpath('C:\\Users\\smcellig\\Desktop\\Project\_Sacha\\edfImport-master');
addpath C:\\toolbox\\Psychtoolbox\\PsychBasic\\MatlabWindowsFilesR2007a\\moglcore.mexw64; % just in case

TMS Initialization
------------------

so = daq.createSession('mcc'); % for TMS pulse
addAnalogOutputChannel(so,'Board0','Ao0','Voltage'); % will change depending on setup of hardware
si = daq.createSession('mcc'); % to get photodiode data
addAnalogInputChannel(si,'Board0','Ai0','Voltage'); % bottom left diode -- (:,2) in diodeData variable
addAnalogInputChannel(si,'Board0','Ai1','Voltage'); % bottom right diode -- (:,3) in diodeData variable

si.Rate = 3333; % the rate that Theresa Desroches used in her experiment
si.IsContinuous = true; % will keep getting diode data until block is over
lh = si.addlistener('DataAvailable',@plotData);
% fid1 = fopen('log1.bin','w'); % In Desroches' script... not even necessary
% lh = si.addlistener('DataAvailable',@(src,event)logData(src, event, fid1));

Get name, write file
--------------------

name = input('What is your name? ','s');
blocksToday = input('How many blocks were completed today? ','s');
blocksToday = num2str(str2num(blocksToday)+1);
full\_filename = \[date '\_Block' blocksToday '\_' name '.xlsx'\];
mkdir(strcat(pwd,'\\',name));
addpath(strcat(pwd,'\\',name));

Screen Initialization
---------------------

stimulusMonitor = 1; % Check settings to determine the proper monitor #
desiredHz = 100;
desiredBits = 32;

\[W,H\] = Screen('WindowSize',stimulusMonitor);

if (Screen('FrameRate',stimulusMonitor)~=desiredHz) % If refresh rate of the monitor doesn't match desired refresh rate...
% %     ResolutionTest(stimulusMonitor); % gives compatible configurations (for Window2)
    % ...change the resolution
    oldRes = SetResolution(stimulusMonitor,W,H,desiredHz,desiredBits); % ..ion(screen #, pixels W, pixels H, Hz, pixel size);
end

percentOfTotal=0.51; % keep within the 0.49-0.51 range --> used to change Background\_Color and gabor texture background
Background\_Color = percentOfTotal\*\[255,255,255\]; % Carrasco et al. 2012 specify no exact background color, but this is good for the gabors
PsychDefaultSetup(1);
Screen('Preference', 'SkipSyncTests', 0);
dummymode=0;       % set to 1 to initialize in dummymode

\[window1,rect\] = Screen('OpenWindow',stimulusMonitor,Background\_Color); % Screen #... may change depending on setup
slack = Screen('GetFlipInterval', window1)/2;
commandwindow;
% Gamma correction
gammaCorrected = input('Has the monitor already been linearized (y/n)? ','s');
if strcmp(gammaCorrected,'n')
    monitor; % do gamma correction
    success % print whether was successful
end

% % % Peter Scarfe stuff % % %
% Query the frame duration
ifi = Screen('GetFlipInterval', window1);
% Perform initial flip to gray background and sync us to the retrace:
vbl = Screen('Flip', window1);
% Numer of frames to wait before re-drawing
waitframes = 1;

Screen Parameters (taken from Iiyama HM204DT-A Manual)
------------------------------------------------------

Width\_of\_Screen = 40.6; % in cm
Height\_of\_Screen = 30.4; % in cm
Distance\_from\_Screen = 62.5; % in cm

More params
-----------

dot\_size = 10; % size of dots in pixels
dot\_colour = \[0,0,0\];% Colour of the dots
dot\_spacing = 2;% Space between the dots in degrees

tmsTimes = \[0.150, 0.200, 0.250\];
str = "Which post-cue TMS delay?:" + "\\n" + "1) 160ms" + "\\n" + "2) 200ms" + "\\n" + "3) 250ms" + "\\n" + "--> ";
A = char(compose(str));

Num\_Trials = 1+str2num(input('How many trials for this block? ','s')); % +1 because the first trial will be voided
TMS\_location = input('Location of TMS? (L4, L8, R4, R8) ','s');
TMS\_output = str2num(input('What percent of TMS output? ', 's'));
tmsTimePostCueOLD = tmsTimes(str2num(input(A,'s'))); % Time after cue to deliver TMS pulse (seconds)

Eyelink Stuff
-------------

stopkey=KbName('space');

Eyelink('Initialize');

el=EyelinkInitDefaults(window1);

% Initialization of the connection with the Eyelink Gazetracker.
% exit program if this fails.
if ~EyelinkInit(dummymode, 1)
    fprintf('Eyelink Init aborted.\\n');
    cleanup;  % cleanup function
    return;
end

\[v vs\] = Eyelink('GetTrackerVersion');
fprintf('Running experiment on a ''%s'' tracker.\\n', vs );

% Make sure that we get gaze data from the Eyelink
Eyelink('Command', 'link\_sample\_data = LEFT,RIGHT,GAZE,AREA');

% Open file to record data to
dir(\[strcat(pwd,'\\',name) '/\*.xlsx'\]);
edfFile = strcat(name,1+num2str(size(dir(\[strcat(pwd,'\\',name) '/\*.edf'\]),1)),'.edf') % 'name' must be less than 8 characters!!!
Eyelink('Openfile', edfFile);

% STEP 4
% Calibrate the eye tracker
EyelinkDoTrackerSetup(el);

% Do a final check of calibration using driftcorrection
EyelinkDoDriftCorrection(el);

% STEP 5
% Start recording eye position
Eyelink('StartRecording');
eyelinkTime1 = EXGetEyeLinkTime;
% Eyelink('Message', 'SYNCTIME');
stopkey=KbName('space');

Screen('FillRect', el.window, Background\_Color);
Screen('TextFont', el.window, el.msgfont);
Screen('TextSize', el.window, el.msgfontsize);
\[width, height\]=Screen('WindowSize', el.window);
message='';
Screen('DrawText', el.window, message, 200, height-el.msgfontsize-20, el.msgfontcolour);
Screen('Flip',  el.window, \[\], 1);

Variable initialization
-----------------------

eye\_used = 0; % Eyelink stuff... (=left eye), the eye coordinates come from this one
sacc\_limit = 4; % what the change in horizontal eye position needs to be to be called a saccade
false = 0;

global diodeData;
diodeData=\[\]; % will be used to read the data from photodiode... MUST be global due to the nature of the callback function used in the listener

x=0;
y=0;
j=1; % used in the while loop to generate trials

responses = cell(1,Num\_Trials); % will be used to keep track of responses

% Convert from visual angle to pixels (ang2pix = function I made to do this)
% Below are the values used to create the boxes inside of which the gabors
% will be drawn (exact values per Carrasco et al. 2012)
value = round(ang2pix(Width\_of\_Screen,W,Distance\_from\_Screen,5)+ang2pix(Width\_of\_Screen,W,Distance\_from\_Screen,6.8));
dot\_placement\_height = ang2pix(Width\_of\_Screen,W,Distance\_from\_Screen,2.5);
dot\_placement\_x = ang2pix(Width\_of\_Screen,W,Distance\_from\_Screen,4); % 4deg left and right of fixation
box\_side\_length = ang2pix(Width\_of\_Screen,W,Distance\_from\_Screen,5); % 5deg length of box side

% Allows for vectorized drawing of boxes (faster!)
dots = \[(W/2)+dot\_placement\_x,(H/2)+dot\_placement\_height;(W/2)+dot\_placement\_x,(H/2)-dot\_placement\_height;...
       (W/2)+dot\_placement\_x+box\_side\_length,(H/2)+dot\_placement\_height;(W/2)+dot\_placement\_x+box\_side\_length,(H/2)-dot\_placement\_height;...
       (W/2)-dot\_placement\_x,(H/2)+dot\_placement\_height;(W/2)-dot\_placement\_x,(H/2)-dot\_placement\_height;(W/2)-dot\_placement\_x-box\_side\_length,(H/2)+dot\_placement\_height;...
       (W/2)-dot\_placement\_x-box\_side\_length,(H/2)-dot\_placement\_height\];

Create all the gabors beforehand (faster!)
------------------------------------------

Initialization of matrices which will contain the necessary parameters to generate the standard and test gabors

propmatTest = zeros(Num\_Trials,8);
propmatStandard = zeros(Num\_Trials,8);
orientation\_standard = zeros(1,Num\_Trials);
orientation\_test = zeros(1,Num\_Trials);
contrast\_test = zeros(1,Num\_Trials);
side = zeros(1,Num\_Trials); % 1 = Left, 2 = Right

cueTimes = \[0.010, 0.060, 0.110, 0.160, 0.210\]; % How long after cue until the stimulus will be drawn, in 50ms steps from 10-210ms (Carrasco et al. 2012)
% contrastValues = \[0.056, 0.112, 0.168, 0.224, 0.3355, 0.447, 0.5585\]; % comes from Fig.6C of Carrasco et al. 2012
contrastValues = 0.01\*\[7.9, 11.1726, 15.8, 22.4, 31.6, 44.6546, 63.1\]; % comes from converting values in Fig.2E to log space

% peakContrastInPixelLuminance = Background\_Color(1)+(contrastValues\*Background\_Color(1)/2); % https://peerj.com/questions/1736-what-was-the-contrast-of-the-gabor/
% troughContrastInPixelLuminance = Background\_Color(1)-(contrastValues\*Background\_Color(1)/2);
pixelsPerDeg = ang2pix(Width\_of\_Screen,W,Distance\_from\_Screen,1);
pointFive = pixelsPerDeg/2; % could have just assigned it to the Gaussian SD ('sigma') but oh well...

% Gabor Features
gaborDimPix = rect(4)/4; % changes the size of gabor texture... best not to mess with this
sigma = pointFive; % 'Gaussian envelope with 0.5deg SD' (Carrasco et al. 2012)
aspectRatio = 1;
phase = 0 + (360-0).\*rand(1); % 'To avoid aftereffects, we randomized their phase (range of 2pi)' (Carrasco et al. 2012)
freq = \[1/pixelsPerDeg, 1.5/pixelsPerDeg\]; % Spatial Freq was 1 or 1.5cpd (Carrasco et al. 2012) --> freq must be in Cycles per Pixel
backgroundOffset = percentOfTotal\*\[1 1 1 0.0\]; % To match the background luminance of 128 (0.5 \* 255 == 128)
%
% CreateProceduralGabor.m
% "If you set the 'disableNorm' parameter to 1 to disable the builtin normf
% normalization and then specify contrastPreMultiplicator = 0.5 then the
% per gabor 'contrast' value will correspond to what practitioners of the
% field usually understand to be the contrast value of a gabor. Specifically,
% assuming a 0.5 (=50%) gray background and a properly gamma corrected /
% linearized display, the 'contrast' value, as described below, that you
% pass to Screen('DrawTexture',...) will then allow to directly specify
% Michelson contrast: 'contrast' = (Imax - Imin) / (Imin + Imax)
% of course assuming isolated, non-superimposing gabors, so the Michelson
% contrast corresponds to the maxima and minima of the gabor patch under
% a suitable phase shift, where the minimum or maximum of the patch lies
% in the center of the patch."
%
disableNorm = 1;
preContrastMultiplier = 0.5;
gabortex = CreateProceduralGabor(window1,(W/4), H/2, \[\], backgroundOffset, disableNorm, preContrastMultiplier);
%%%%%%
for i = 1:Num\_Trials

    % Standard Contrast
    chosenFreq = freq(randi(numel(freq)));
    propmatStandard(i,:) = \[phase, chosenFreq, sigma, 0.224, aspectRatio, 0, 0, 0\]; % for the standard gabor

    a = -1 +(2).\*rand(1);
    Sign = sign(a);
    orientation\_standard(i) = Sign\*45;
    contrast\_standard = 0.224;
    a = -1 +(2).\*rand(1);
    sign1 = sign(a);
%     o = sign1\*normrnd(11.7,0.8); % 'Orientation difference between test and standard stimulus was 11.7 +- 0.8deg' (Carrasco et al. 2012)
    o = sign1\*10; % Experiment 3: 'The test stimulus orientation was irrelevant to the observer, but randomly +-10deg off the standard's orientation' (Carrasco et al. 2012)

    % Test Stimuli
% %     a = -1 +(2).\*rand(1); % equally likely to be + or -
% %     sign1 = sign(a); % take the sign of 'a'
% %     c = sign1\*(0.1 + (0.2-0.1).\*rand(1)); % use the sign of 'a' to make the change in contrast positive or negative

NOTE: Carrasco used contrast deviations that were a 'range of 0.9
-----------------------------------------------------------------

log units in seven equidistant steps around standard contrast')...
------------------------------------------------------------------

This it not what I did because I am not sure which way to interpret
-------------------------------------------------------------------

that
----

    orientation\_test(i) = (Sign\*(45+o)); % keep the same sign as standard gabor orientation, but +-10deg
% %     contrast\_test(i) = 0.224+c; % test gabor contrast == standard gabor contrast +- a certain value
    n=randperm(numel(contrastValues),1);
    contrast\_test(i) = contrastValues(n);
    side(i) = round(1 + (2-1).\*rand(1)); % 1 (left) or 2 (right)
    propmatTest(i,:) = \[phase, chosenFreq, sigma, contrast\_test(i), aspectRatio, 0, 0, 0\]; % each row of this matrix represents a different gabor

end

% Gabor position bounds (best not to mess with this, the calculation is really strange)
%    - the constant will shift them right or left, use this according to
%      eccentricity of stimulus
%        --> The original position is based on an ecc. of 10deg, so I am
%            shifting it here by 2deg since the new position is 8deg

w1 = (round(-value/4))+ang2pix(Width\_of\_Screen,W,Distance\_from\_Screen,6); % lower bound (left)
w2 = ((W/2)-(round(value/4)))+ang2pix(Width\_of\_Screen,W,Distance\_from\_Screen,6); % upper bound (left)
w3 = ((W/2+value/2)-value/4)-ang2pix(Width\_of\_Screen,W,Distance\_from\_Screen,6); % lower bound (right)
w4 = ((W+value/2)-value/4)-ang2pix(Width\_of\_Screen,W,Distance\_from\_Screen,6); % upper bound (right)

% % % % Quick test of gabors in For-Loop
% for x = 1:Num\_Trials
%     Screen('Flip',window1,vbl + (waitframes - 0.5) \* ifi);
% %     WaitSecs(0.2);
%     Screen('DrawTextures', window1, gabortex, \[\], \[w1 0 w2 (H)\], orientation\_test(x), \[\], \[\], \[\], \[\], 2, propmatTest(x,:)');
%     Screen('Flip',window1,vbl + (waitframes - 0.5) \* ifi);
% %     WaitSecs(1);
% end

Create Textures (allows for fast switch of screen)
--------------------------------------------------

Beeper(600, 0.2, 0.5);
%%%%%%%%%% FIXATION SCREEN %%%%%%%%%%%
Screen('DrawDots',window1,\[(W/2),(H/2)\],10,\[0 0 0\],\[\],1);
Screen('DrawDots',window1,\[(W/2),(H/2)\],3,\[255 255 255\],\[\],1);
% Draw boxes
for i = 1:length(dots)
    Screen('DrawDots',window1,\[dots(i,1),dots(i,2)\],3,\[0 0 0\],\[\],1);
end
% Screen('FillRect',window1,\[255 255 255\],\[0 H-70 70 H\]);
Screen('Flip', window1);

center = Screen('GetImage',window1,\[((W/2)-10) ((H/2)-10) ((W/2)+10) ((H/2)+10)\]);
top = Screen('GetImage',window1,\[(0) ((H/2)+dot\_placement\_height - 10) (W) ((H/2)+dot\_placement\_height + 10)\]);
topDots = Screen('MakeTexture',window1,top);
centerDot = Screen('MakeTexture',window1,center);
A = Screen('GetImage',window1);
normalFixation = Screen('MakeTexture',window1,A);

Beeper(600, 0.2, 0.5);
%%%%%%%%%%%%%%% LEFT CUE %%%%%%%%%%%%%%%%%

Draw fixation w/ left-pointing cue
----------------------------------

Screen('DrawDots',window1,\[(W/2),(H/2)\],10,\[0 0 0\],\[\],1);
Screen('DrawLine',window1,\[0,0,0\],(W/2)-20,(H/2),(W/2),(H/2),3);
Screen('DrawDots',window1,\[(W/2),(H/2)\],3,\[255 255 255\],\[\],1);

Draw boxes
----------

Screen('DrawDots',window1,\[(W/2),(H/2)\],10,\[0 0 0\],\[\],1);
Screen('DrawDots',window1,\[(W/2),(H/2)\],3,\[255 255 255\],\[\],1);
% Draw boxes
for i = 1:length(dots)
    Screen('DrawDots',window1,\[dots(i,1),dots(i,2)\],3,\[0 0 0\],\[\],1);
end
Screen('Flip', window1);

L = Screen('GetImage',window1);
leftCue = Screen('MakeTexture',window1,L);

Beeper(600, 0.2, \[0.5\]);

%%%%%%%%%%%%%%% RIGHT CUE %%%%%%%%%%%%%%%%%

Draw fixation w/ right-pointing cue
-----------------------------------

Screen('DrawDots',window1,\[(W/2),(H/2)\],10,\[0 0 0\],\[\],1);
Screen('DrawLine',window1,\[0,0,0\],(W/2)+20,(H/2),(W/2),(H/2),3);
Screen('DrawDots',window1,\[(W/2),(H/2)\],3,\[255 255 255\],\[\],1);

Draw boxes
----------

Screen('DrawDots',window1,\[(W/2)+dot\_placement\_x,(H/2)+dot\_placement\_height\],3,\[0 0 0\],\[\],1);
Screen('DrawDots',window1,\[(W/2)+dot\_placement\_x,(H/2)-dot\_placement\_height\],3,\[0 0 0\],\[\],1);
Screen('DrawDots',window1,\[(W/2)+dot\_placement\_x+box\_side\_length,(H/2)+dot\_placement\_height\],3,\[0 0 0\],\[\],1);
Screen('DrawDots',window1,\[(W/2)+dot\_placement\_x+box\_side\_length,(H/2)-dot\_placement\_height\],3,\[0 0 0\],\[\],1);

Screen('DrawDots',window1,\[(W/2)-dot\_placement\_x,(H/2)+dot\_placement\_height\],3,\[0 0 0\],\[\],1);
Screen('DrawDots',window1,\[(W/2)-dot\_placement\_x,(H/2)-dot\_placement\_height\],3,\[0 0 0\],\[\],1);
Screen('DrawDots',window1,\[(W/2)-dot\_placement\_x-box\_side\_length,(H/2)+dot\_placement\_height\],3,\[0 0 0\],\[\],1);
Screen('DrawDots',window1,\[(W/2)-dot\_placement\_x-box\_side\_length,(H/2)-dot\_placement\_height\],3,\[0 0 0\],\[\],1);
Screen('Flip', window1);

R = Screen('GetImage',window1);
rightCue = Screen('MakeTexture',window1,R);
% % % % % % % % % % % % % % % % % % % % % %

Experiment about to start
-------------------------

Screen('FillRect',window1, \[0 0 0\],\[0 H-100 100 H\]); % Draw black box in bottom left corner
Screen('Flip', window1, vbl + (waitframes - 0.5) \* ifi);
WaitSecs(3);
pause on;

% Initialize data structures to contain time stamps
stimOffset = zeros(1,Num\_Trials);
stimOnset =zeros(1,Num\_Trials);
fixation = zeros(1,Num\_Trials);
cue = zeros(1,Num\_Trials);
standard = zeros(1,Num\_Trials);
standardOff = zeros(1,Num\_Trials);

stamps = zeros(Num\_Trials,5);
stimOnsetSTAMP = zeros(1,Num\_Trials);
cueSTAMP = zeros(1,Num\_Trials);
tmsSTAMP = zeros(1,Num\_Trials);
stimOffsetSTAMP = zeros(1,Num\_Trials);
saccSTAMP = zeros(1,Num\_Trials);
cueTime = zeros(1,Num\_Trials);

TMSbinary = zeros(1,Num\_Trials);

Beeper(800,0.8,0.7); % beep to indicate start of block

si.startBackground(); % start getting data from photodiode
% % % % delete(lh);
% % % % close(fid1);

Task
----

while j~=Num\_Trials+1

    Beeper(800,1,0.05); % "Trial j is starting!"
    outputSingleScan(so,0) % make sure TMS ttl is off
    false = 0;
    tmsTimePostCue = tmsTimePostCueOLD+(sign(orientation\_test(j)))\*((0.025).\*rand(1));
    if side(j)==1
       varname = genvarname('leftCue');
    else
       varname = genvarname('rightCue');
    end

Fixation
--------

Draw Fixation Point

    Screen('DrawDots',window1,\[(W/2),(H/2)\],10,\[0 0 0\],\[\],1);
    Screen('DrawDots',window1,\[(W/2),(H/2)\],3,\[255 0 0\],\[\],1);
    % Draw boxes
    for i = 1:length(dots)
        Screen('DrawDots',window1,\[dots(i,1),dots(i,2)\],3,\[0 0 0\],\[\],1);
    end
    Screen('FillRect',window1,\[0 0 0\],\[0 H-100 100 H\]); % Draw black box in bottom left corner
    Screen('Flip', window1, vbl + (waitframes - 0.5) \* ifi);
% % %     WaitSecs(0.2);
    T=tic;
    myCoordList=\[\]; % have to reinitialize to avoid comparing the last coordinates from previous trial
    saccade=0;
    while (saccade==0) && (toc(T)<1) % make sure subject doesn't do a saccade prematurely (make sure they fixate before stimuli show up) (Carrasco et al. 2012)
        \[saccade, myCoordList\] = checkSaccade(myCoordList,sacc\_limit);
        if (saccade==1)
            disp(' ');
            disp('Saccade detected during fixation... Trial voided');
            false=1; % will restart this iteration after trial
        end
    end

Standard
--------

    Screen('DrawTextures',window1,normalFixation); % draw fixation
    Screen('FillRect',window1,\[0 0 0\],\[0 H-100 100 H\]); % Draw black box in bottom left corner
    Screen('Flip', window1, vbl + (waitframes - 0.5) \* ifi);

    time = 0.250 + (0.750-0.250).\*rand(1); % ranged from 250-750ms between fixation and drawing of stimuli (Carrasco et al. 2012)
    t = EXGetEyeLinkTime;
    % Left
    Screen('DrawTextures', window1, gabortex, \[\], \[w1 0 w2 H\], orientation\_standard(j), \[\], \[\], \[\], \[\], kPsychDontDoRotation, propmatStandard(j,:)');
    % Right
    Screen('DrawTextures', window1, gabortex, \[\], \[w3 0 w4 H\], orientation\_standard(j), \[\], \[\], \[\], \[\], kPsychDontDoRotation, propmatStandard(j,:)');

Draw fixation
-------------

    Screen('DrawDots',window1,\[(W/2),(H/2)\],10,\[0 0 0\],\[\],1);
    Screen('DrawDots',window1,\[(W/2),(H/2)\],3,\[255 255 255\],\[\],1);

    for i = 1:length(dots)
        Screen('DrawDots',window1,\[dots(i,1),dots(i,2)\],3,\[0 0 0\],\[\],1);
    end
    Screen('FillRect',window1,\[0 0 0\],\[0 H-100 100 H\]); % Draw black box in bottom left corner
    done = 0;
    while done == 0
        if (EXGetEyeLinkTime-t >= 300\*time)
            \[VBLstndOff, standard(j)\] = Screen('Flip', window1, vbl + (waitframes - 0.5) \* ifi);
            t = EXGetEyeLinkTime;
            done = 1;
        end
    end
    done=0;
%     start = EXGetEyeLinkTime;
    while done == 0
        if (EXGetEyeLinkTime-t >= 50) % standard gabors only up for 50ms
            Screen('DrawTextures',window1,normalFixation);
            Screen('FillRect',window1,\[0 0 0\],\[0 H-100 100 H\]); % Draw black box in bottom left corner
            \[VBLstndOff, standardOff(j)\] = Screen('Flip', window1, vbl + (waitframes - 0.5) \* ifi);
            done = 1;
        end
    end

Fixation
--------

    pause(0.450); % 450ms between standard gabors disappearing and cue onset

Cue
---

    if (side(j)==1) % Left
        Screen('DrawTextures',window1,leftCue);
        \[VBLTimestamp, cue(j)\] = Screen('Flip', window1, vbl + (waitframes - 0.5) \* ifi);
        cueSTAMP(j) = EXGetEyeLinkTime;
    else % Right
        Screen('DrawTextures',window1,rightCue);
        \[VBLTimestamp, cue(j)\] = Screen('Flip', window1, vbl + (waitframes - 0.5) \* ifi);
        cueSTAMP(j) = EXGetEyeLinkTime;
    end

Stimuli
-------

    number = 1 + (2-1).\*rand(1) - 1;
    if number > 0.333
        TMSbinary(j) = 1;
    end
    saccade=0;
    done=0;
    zero=0;
    one=0;
    two=0;
    myCoordList=\[\];
    cueTime(j)=1000\*cueTimes(randi(numel(cueTimes)));
    startRecording = EXGetEyeLinkTime;
    while done==0
        evt = Eyelink('NewestFloatSample'); % keep getting eye data
        x = evt.gx(1); % only need x position since stimuli are presented horizontally
        if isempty(myCoordList) < 1
            if (abs(myCoordList(end,1)-x) > sacc\_limit) && (saccade==0) % if the saccade threshold is crossed, then do a saccade stamp
                saccSTAMP(j) = evt.time;
% saccSTAMP(j) = EXGetEyeLinkTime;
                saccade=1;

            elseif (EXGetEyeLinkTime-cueSTAMP(j) >= 1000\*tmsTimePostCue) && (zero==0) && (TMSbinary(j) == 1) % if the time since the cue passes the inputted TMS time, then give a pulse!
                tmsSTAMP(j) = EXGetEyeLinkTime;
                outputSingleScan(so,4);
                outputSingleScan(so,0);
                zero=1; % stop the loop from happening again (must do >= NOT == in the If-Loop because it may not be able to check at the same level of precision as is required by the == operator)

            elseif (EXGetEyeLinkTime-cueSTAMP(j) >= cueTime(j)) && (one==0) % if the time since the cue passes the generated cue-stimulus delay, draw the test gabor
                if side(j) == 1

Draw fixation w/ left-pointing cue
----------------------------------

                    Screen('DrawDots',window1,\[(W/2),(H/2)\],10,\[0 0 0\],\[\],1);
                    Screen('DrawLine',window1,\[0,0,0\],(W/2)-20,(H/2),(W/2),(H/2),3);
                    Screen('DrawDots',window1,\[(W/2),(H/2)\],3,\[255 255 255\],\[\],1);

Draw gabor
----------

                    Screen('DrawTextures', window1, gabortex, \[\], \[w1 0 w2 H\], orientation\_test(j), \[\], \[\], \[\], \[\], kPsychDontDoRotation, propmatTest(j,:)');
                else

Draw fixation w/ right-pointing cue
-----------------------------------

                    Screen('DrawDots',window1,\[(W/2),(H/2)\],10,\[0 0 0\],\[\],1);
                    Screen('DrawLine',window1,\[0,0,0\],(W/2)+20,(H/2),(W/2),(H/2),3);
                    Screen('DrawDots',window1,\[(W/2),(H/2)\],3,\[255 255 255\],\[\],1);

Draw gabor
----------

                    Screen('DrawTextures', window1, gabortex, \[\], \[w3 0 w4 H\], orientation\_test(j), \[\], \[\], \[\], \[\], kPsychDontDoRotation, propmatTest(j,:)');
                end

Draw boxes
----------

                for i = 1:length(dots)
                    Screen('DrawDots',window1,\[dots(i,1),dots(i,2)\],3,\[0 0 0\],\[\],1);
                end
                Screen('FillRect',window1,\[0 0 0\],\[0 H-100 100 H\]); % Draw black box in bottom left corner
                \[VBLTimestamp, stimOnset(j)\] = Screen('Flip', window1, vbl + (waitframes - 0.5) \* ifi);
                stimOnsetSTAMP(j) = EXGetEyeLinkTime; % there will be some latency between Screen('Flip') actually flipping and claiming it's done, which is why to use diode data
                one=1; % will only run once

            elseif (one==1) && (EXGetEyeLinkTime-stimOnsetSTAMP(j)>=40) && (two==0) % if the stimulus has been up for 50ms, clear it
                Screen('DrawTextures',window1,eval(varname)); % NOTE: Carrasco et al. 2012 drew the same cue as was up before, but this will be slower since it requires 2 If-Statements (checking which side the cue should draw)
                \[VBLTimestamp, stimOffset(j)\] = Screen('Flip',window1,vbl + (waitframes - 0.5) \* ifi);
%                  stimOffsetSTAMP(j) = EXGetEyeLinkTime;
                stimOffsetSTAMP(j) = stimOnsetSTAMP(j)+(stimOffset(j)-stimOnset(j));
                two=1;
            end
        end
        myCoordList=\[x,y\];
        if (EXGetEyeLinkTime-startRecording >=400) % if they don't saccade within 400ms, void the trial
            done=1;
            if saccade==0
               false=1;
               disp(' ');
               disp("Trial voided... Subject didn't saccade in time");
            end
        end
    end
    % Keep track of the timestamps
    stamps(j,:) = \[stimOnsetSTAMP(j), cueSTAMP(j), tmsSTAMP(j), stimOffsetSTAMP(j), saccSTAMP(j)\];

Ask which one
-------------

    pass=0;
    num=0;
    while pass==0 % Make sure response is valid
        commandwindow;
        if num==1
            disp(' ');
            disp('Invalid response: please try again');
        end
        disp(' ');
%         disp('Row (5-6 and 2-3) indicates relative contrast');
%         disp('Column (5-2 and 6-3) indicates relative orientation');
%         get\_ans = input('Please indicate the relative orientation and contrast: ','s');
        get\_ans = input('Higher (s/5) or lower (x/2) relative contrast?: ','s'); % NOTE: this is different from Carrasco et al. 2012, where they had users report gabors on right with 5,2 and gabors on left with S,X
        responses{j} = get\_ans;
        if (length(get\_ans)==1) && (mean(strcmp(get\_ans,{'x','s','5','2'}))>0)
            pass=1;
        end
        num=1;
    end

    if false==1 % If they breached one of the stipulations, then void the trial and switch up features of stimulus except for contrast
        j=j+0;
        stamps(j,:) = \[0 0 0 0 0\];
        orientation\_standard(j) = -1\*orientation\_standard(j); % or you can randomize next placement... somehow
        orientation\_test(j) = -1\*orientation\_test(j);
        side(j) = round(1 + (2-1).\*rand(1));
    else
        j=j+1;
    end

end
Beeper(200,100,0.7); % beep to indicate end of block
sca; % Close window:
stop(si); % stop checking photodiode data
delete(lh); % delete listener

% % % %% Close up recording, etc.
Eyelink('StopRecording');
Eyelink('CloseFile');
% % %
% % % % tmsTimesRelSaccade = tmsSTAMP-saccSTAMP; % test offset times rel. saccade
% % %
% Download data file
disp(\[' '\]);
try
    fprintf('Receiving data file ''%s''\\n', edfFile);
    status=Eyelink('ReceiveFile',edfFile,strcat(pwd,'\\',name),1);
    if status > 0
        fprintf('ReceiveFile status %d\\n', status);
    end
    if 2==exist(edfFile, 'file')
        fprintf('Data file ''%s'' can be found in ''%s''\\n', edfFile, strcat(pwd,'\\',name) );
    end
catch rdf
    fprintf('Problem receiving data file ''%s''\\n', edfFile );
    rdf;
end
Eyelink('Shutdown');

Photodiode Stuff
----------------

% % stampON = \[\]; % % for i = 100:(length(diodeData)) % % if (diodeData(i,2)>=-1) && (all(diodeData(i-100:i-1,2)<-1.4)) % % stampON=\[stampON;diodeData(i,1)\]; % % end % % end % % % % tempDiodeData = \[flipud(diodeData(:,1)),flipud(diodeData(:,2))\]; % % stampOFF = \[\]; % % for i = 101:(length(tempDiodeData)) % % if (tempDiodeData(i,2)>=-1) && (all(tempDiodeData(i-100:i-1,2)<-1.4)) % % stampOFF=\[stampOFF;tempDiodeData(i,1)\]; % % end % % end % % stampOFF=flipud(stampOFF); =================== 'stampON' will give all the times that the corner switched to grey (blank) 'stampOFF' will give all the times that the corner switched back to black See plot for a clear picture Format of the diode markers: - black when trial starts - even numbered stampOFF indices are start of trial (bc first won't be included since it starts at black) - grey when cue is up - odd numbered stampON indices are cue onset - black when stimulus is up - odd numbered stampOFF indices are stimulus onset - grey when stimulus disappears and normal fixation screen is redrawn - even numbered stampON indices are stimulus offset =================== % % figure(1) % % plot(diodeData(:,1),diodeData(:,2)); % % hold on % % for j = 1:length(stampON) % % for i = 1:length(diodeData) % % if diodeData(i,1)==stampON(j) % % scatter(diodeData(i,1),diodeData(i,2),'rx'); % % end % % end % % end % % for j = 1:length(stampOFF) % % for i = 1:length(diodeData) % % if diodeData(i,1)==stampOFF(j) % % scatter(diodeData(i,1),diodeData(i,2),'kx'); % % end % % end % % end

Write Excel
-----------

results=zeros(1,Num\_Trials);
orientationAnswers=\[\];
contrastAnswers=\[\];
answers={};
highContrast=zeros(1,Num\_Trials);

details = {name; date; 'Gabor'; strcat(num2str(Distance\_from\_Screen),'cm'); TMS\_location; strcat('TMS time post-cue: ',num2str(100\*tmsTimePostCueOLD),'ms'); strcat('TMS output: ',num2str(TMS\_output),'%'); 'Saccade'};

for j = 1:numel(details)
    RangeA = \['A' num2str(j)\];
    xlswrite2(strcat(pwd,'\\',name,'\\',full\_filename),details(j),1,RangeA);
end

abc = char(97:122);
headers = {'Actual','Reported','Correct?',' ','Test Orient.','Test Contrast','Test Onset','Cue Onset','TMS pulse','Test Offset','Saccade Det.','Reported Higher Contrast','Side','TMS?'};

for i = 1:length(headers)
     xlswrite2(strcat(pwd,'\\',name,'\\',full\_filename),headers(i),1,\[abc(i+2)\]);
end

% % % %  Sections below commented out because orientation is no longer a
% % % %  factor (Experiment 3)
for j = 1:Num\_Trials
% % %     orientationAnswers = \[orientationAnswers; orientation\_test(j)>orientation\_standard(j)\];  % 1 means Test was CCW to Standard (and 0 means Test was CW to Standard... duh)
    contrastAnswers = \[contrastAnswers; contrast\_test(j)>contrast\_standard\]; % 1 means Test had higher contrast than Standard

    if strcmp(responses{j},'5')==1 || strcmp(responses{j},'s')==1
    	highContrast(j)=1;
    end

    if contrastAnswers(j)==1 && (side(j)==2)
       answers{j} = '5';
    end
    if contrastAnswers(j)==0 && (side(j)==2)
        answers{j} = '2';
    end
    if contrastAnswers(j)==1 && (side(j)==1)
       answers{j} = 's';
    end
    if contrastAnswers(j)==0 && (side(j)==1)
        answers{j} = 'x';
    end
% % % %     if (orientationAnswers(j)==1) && (contrastAnswers(j)==1)
% % % %         answers = \[answers; 5\];
% % % %     end
% % % %     if (orientationAnswers(j)==0) && (contrastAnswers(j)==1)
% % % %         answers = \[answers; 6\];
% % % %     end
% % % %     if (orientationAnswers(j)==0) && (contrastAnswers(j)==0)
% % % %         answers = \[answers; 3\];
% % % %     end
% % % %     if (orientationAnswers(j)==1) && (contrastAnswers(j)==0)
% % % %         answers = \[answers; 2\];
% % % %     end

    results(j) = strcmp(answers{j},responses{j});
    Range0=\['C' num2str(j+1)\];
    xlswrite2(strcat(pwd,'\\',name,'\\',full\_filename),answers(j),1,Range0);
    Range1=\['D' num2str(j+1)\];
    xlswrite2(strcat(pwd,'\\',name,'\\',full\_filename),responses{j},1,Range1);
    Range2=\['E' num2str(j+1)\];
    xlswrite2(strcat(pwd,'\\',name,'\\',full\_filename),results(j),1,Range2); % write in results
    Range3=\['G' num2str(j+1)\];
    xlswrite2(strcat(pwd,'\\',name,'\\',full\_filename),orientation\_test(j),1,Range3);
    Range4=\['H' num2str(j+1)\];
    xlswrite2(strcat(pwd,'\\',name,'\\',full\_filename),contrast\_test(j),1,Range4);
    Range5=\['I' num2str(j+1)\];
    xlswrite2(strcat(pwd,'\\',name,'\\',full\_filename),stamps(j,:),1,Range5);
    Range6=\['N' num2str(j+1)\];
    xlswrite2(strcat(pwd,'\\',name,'\\',full\_filename),highContrast(j),1,Range6);
    Range7=\['O' num2str(j+1)\];
    xlswrite2(strcat(pwd,'\\',name,'\\',full\_filename),side(j),1,Range7);
    Range8=\['P' num2str(j+1)\];
    xlswrite2(strcat(pwd,'\\',name,'\\',full\_filename),TMSbinary(j),1,Range8);
%     Range6=\['M' num2str(j)\];
%     xlswrite(full\_filename,timeAfterCue(j),1,Range6);
%     Range5=\['H' num2str(j)\];
%     xlswrite(full\_filename,datestr(now),1,Range5);
end
% Restore keyboard output to Matlab:
ListenChar(0);
disp(\['Score for this block: ',num2str(100\*sum(results)/length(results)),'%'\]);
% % %

Eyelink data
------------

% % %% Get Eyelink/eye position data (post-hoc)

eyeData = edfImport(strcat(pwd,'\\',name,'\\',edfFile),\[1 0 1\],'time px',0);
offset = double(eyelinkTime1-eyeData.Samples.time(1)); % the variable "eyelinkTime1" is assigned after the Eyelink has started recording... offset this difference in the time series
%                                                      NOTE: that first
%                                                      time stamp of the
%                                                      Eyelink is not
%                                                      accessible until
%                                                      afterwards, hence
%                                                      the absence in the
%                                                      live software...
%                                                      Adjustments must be
%                                                      made retroactively
points1 = zeros(1,Num\_Trials);
points2 = zeros(1,Num\_Trials);
points3 = zeros(1,Num\_Trials);
points4 = zeros(1,Num\_Trials);
points5 = zeros(1,Num\_Trials);

figure(2)
plot(1:length(eyeData.Samples.px(1,:)),eyeData.Samples.px(1,:)+6000,'b-');
hold on
for i = 1:Num\_Trials
    points1(i) = \[eyeData.Samples.px(1,round(offset+stimOnsetSTAMP(i)-eyelinkTime1))\];
    points2(i) = \[eyeData.Samples.px(1,round(offset+cueSTAMP(i)-eyelinkTime1))\];
    points3(i) = \[eyeData.Samples.px(1,round(offset+tmsSTAMP(i)-eyelinkTime1))\];
    points4(i) = \[eyeData.Samples.px(1,round(offset+stimOffsetSTAMP(i)-eyelinkTime1))\];
    points5(i) = \[eyeData.Samples.px(1,round(offset+saccSTAMP(i)-eyelinkTime1))\];

    scatter((offset+stimOnsetSTAMP(i)-eyelinkTime1),points1(i)+6000,'rx');
    scatter(offset+cueSTAMP(i)-eyelinkTime1,points2(i)+6000,'kx');
    scatter(offset+tmsSTAMP(i)-eyelinkTime1,points3(i)+6000,'gx');
    scatter(offset+stimOffsetSTAMP(i)-eyelinkTime1,points4(i)+6000,'mx');
    scatter(offset+saccSTAMP(i)-eyelinkTime1,points5(i)+6000,'cx');
    scatter(offset+stimOnsetSTAMP(i)-eyelinkTime1,points1(i)+6000,'ro');
    scatter(offset+cueSTAMP(i)-eyelinkTime1,points2(i)+6000,'ko');
    scatter(offset+tmsSTAMP(i)-eyelinkTime1,points3(i)+6000,'go');
    scatter(offset+stimOffsetSTAMP(i)-eyelinkTime1,points4(i)+6000,'mo');
    scatter(offset+saccSTAMP(i)-eyelinkTime1,points5(i)+6000,'co');
end

xlabel('Time (secs)');
ylabel('Gaze position');
title('Horizontal gaze position over time');
legend('Eye position (X)','Stimulus onset','Cue onset','TMS pulse', 'Stimulus Offset', 'Saccade Detected');
xt = get(gca, 'XTick');
set(gca, 'XTick',xt, 'XTickLabel',xt\*1E-3);
set(gca,'XMinorTick','on','YMinorTick','off');

%%%%%%%%%%%%%%%%%%%%%%%%%%%
