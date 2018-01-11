# BucketLights

A simple Arduino project to coordinate multiple NeoPixel lights with various patterns.
Just hook up the strips, assign a meaning to them, hook up the Ardiuno to a serial port and
send the commands.

The original concept was used on the Bit Buckets' 2017 Robot, Marvin, to play the FIRST Robotics
Competition (FRC) game, Steamworks. The lights were coordinated to the states of four (4) subsystems
and their associated states.

The hookup is just a matter of editing the BucketLights.ino file:
    1) LightingObjects enumeration for pin assignments
    2) myStrips array for the NeoPixel strip instances

Use "?" for help:

    String format is simple: 'NFCnbbbpppp'   
        N - Strip Number 0..9   
        F - Function   
            0 (zero) = off   
            1      = Solid ON   
            S      = Snore on 3 second period   
            B      = Blink with period pppp msec   
            F      = Forward Chase n pixels (n >= 2, 1 on and n-1 off) with period pppp msec   
            R      = Reverse Change n pixels (n >= 2, 1 on and n-1 off) with period pppp msec   
            C      = Cylon (1-light side-to-side) with update period pppp msec   
            *      = Sparkles (random colors) changing at period pppp msec   
        C - Color Code   
            0 = black (OFF)   
            W = white   
            R = red   
            G = green   
            B = blue   
            C = cyan   
            M = magenta   
            Y = yellow   
            O = orange   
            V = violet   
        n - Used only in F and R functions to space the pixels (ignored in all other modes)   
        bbb - Brightness from 000 to 255   
        pppp - Period in milliseconds between transitions   


Copyright (c) 2017 - RocketRedNeck / Michael Kessel

RocketRedNeck and MIT Licenses

RocketRedNeck hereby grants license for others to copy and modify this source code for
whatever purpose other's deem worthy as long as RocketRedNeck is given credit where
where credit is due and you leave RocketRedNeck out of it for all other nefarious purposes.

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
