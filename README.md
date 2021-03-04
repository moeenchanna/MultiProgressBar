# MultiProgressBar
[![](https://jitpack.io/v/salihselimsekerci/MultiProgressBar.svg)](https://jitpack.io/#salihselimsekerci/MultiProgressBar)
[![Codacy Badge](https://app.codacy.com/project/badge/Grade/c4689c2c33774ef0ac7ce784cc4e3fe2)](https://www.codacy.com/gh/salihselimsekerci/MultiProgressBar/dashboard?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=salihselimsekerci/MultiProgressBar&amp;utm_campaign=Badge_Grade)


![multiprogressbar](https://user-images.githubusercontent.com/53614606/109932377-24ae0b00-7cdb-11eb-9b52-87fc160b4d2e.gif)


## Short description

This library makes it possible to display a progress bar, as in Instagram Stories, without much effort.

View support state recovery using `onSaveInstanceState`

## Details

These attributes (`app` in your layout) allow you to fine-tune the behavior of the progress bar:

1. `lineColor` (color) default: `Color.GRAY`
1. `progressColor` (color) default: `Color.WHITE`
1. `progressSteps` (integer) default: `1`
1. `progressPadding` (dimension) default: `8dp`
1. `progressWidth` (dimension) default: `10F`
1. `progressPercents` (integer) default: `100`
1. `isNeedRestoreProgress` (boolean) default: `false`
1. `singleDisplayedTime` (float) default: `1F`

Also the following api allows you to control the display of progress:

1. `start()` - starts / resumes showing progress
1. `pause()` - pauses showing progress. The scale stops at the current position
1. `previous()` - move to the beginning of the previous block of progress. If progress is started, the show will start immediately. Otherwise, it will stop at the beginning of the block.
1. `next()` - move to the beginning of the next block of progress. If progress is started, the show will start immediately. Otherwise, it will stop at the beginning of the block.
1. `clear()` - clearing the current state of progress, resetting the scale to the very beginning
1. `setListener(listener: ProgressStepChangeListener)` - sets the listener `ProgressStepChangeListener` to switch progress blocks
1. `setProgressPercents(progress: Int` - sets the number of percent for calculating the progress scale
1. `setProgressStepsCount(stepsCount: Int)` - sets the total number of progress steps
1. `setSingleDisplayTime(singleDisplayedTime: Float)` - sets the display time of one cell. Can be used in run time

``` kotlin
interface ProgressStepChangeListener {
    fun onProgressStepChange(newStep: Int)
}
```

## Usage

Artifact is publishing to Jitpack.io. You can add this repository to your project with:
```	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
```

Add to your .gradle file:
```gradle
dependencies {
	        implementation 'com.github.salihselimsekerci:MultiProgressBar:Tag'
	}
```

## Sample

The sample is on `app` module


# License

    MIT License

    Copyright (c) 2021 Salih Selim ŞEKERCİ

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
