# 📼 PHP FFmpeg - Video Streaming

This package utilizes **[FFmpeg](https://ffmpeg.org)**  to bundle media content for online streaming, including DASH and
HLS. Additionally, it provides the capability to implement **[DRM](https://en.wikipedia.org/wiki/Digital_rights_management)** for HLS packaging. The program offers a range of
options to open files from cloud storage and save files to cloud storage as well.

## Documentation

## Basic Usage

```php
use Streaming\Representation;

$r_360p  = (new Representation)->setKiloBitrate(276)->setResize(640, 360);
$r_480p  = (new Representation)->setKiloBitrate(750)->setResize(854, 480);
$r_720p  = (new Representation)->setKiloBitrate(2048)->setResize(1280, 720);

$video->hls()
    ->x264()
    ->addRepresentations([$r_360p, $r_480p, $r_720p])
    ->save();
```


## Contributors (prior to fork)

Your contribution is crucial to our success, regardless of its size. We appreciate your support and encourage you to
read our **[CONTRIBUTING](https://github.com/quasarstream/php-ffmpeg-video-streaming/blob/master/CONTRIBUTING.md)**
guide for detailed instructions on how to get involved. Together, we can make a significant impact.

<a href="https://github.com/quasarstream/php-ffmpeg-video-streaming/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=quasarstream/php-ffmpeg-video-streaming" />
</a>

Made with [contrib.rocks](https://contrib.rocks).

## License

The MIT License (MIT). See **[License File](https://github.com/quasarstream/php-ffmpeg-video-streaming/blob/master/LICENSE)** for more
information.

