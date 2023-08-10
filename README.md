#
<div align="center">

  🆓 Free* video and short content creation with AI 🆓

</div>

<div align="center">
  <div style="display: flex;">
    <img width="300" src="https://github.com/su77ungr/FreeShortGPT/assets/69374354/5701e291-d4b3-497e-aa84-f5c6339884e0" alt="Image 1">
    <img width="300" src="https://github.com/su77ungr/FreeShortGPT/assets/69374354/2b98b086-12cc-4dc0-bebd-c34fb856ad01" alt="Image 2">
  </div>
</div>


</div>


### Installation and Use

For setup refer to the main [repo](https://docs.shortgpt.ai/docs/how-to-install) and installation [guide](https://docs.shortgpt.ai/docs/how-to-install)
### Update 
- includes youtube_api.py without rate time throtteling or oauth authentication errors (we gather streamable with pytube to avoid bans)
- works out of the box without google's YouTube v3 and credentials
- not rate limited like pexels API

### Features 


Inside `api_utils` functions provide utility for working with different APIs. Files: `image_api.py`, `pexels_api.py`,  `youtube_api.py` and `eleven_api.py`. We added  `youtube_api.py` to source video assets directly from YouTube. Feel free to modify `the _generateVideoUrls` function for the hierachy of video asset sources. 

-  #### `search_videos_YouTube(query_string)`
  
      The search_videos_YouTube function takes a query string as input and searches for a video on YouTube based on that query. It returns the URL of the first search result if found, or None if no video is found.
      
      Integration of `shortGPT.api_utils.youtube_api`, which serves as an additional source for gathering footage based on the queried keyword. This is particularly useful when dealing with niche / comedy / meme topics where stock footage is not available. If nothing matches we backtrack to the pexels API. 

-  #### `triage_videos_Youtube(expected_score_parameter)` ❗not released yet

### Demo

demo_new shows the accuracy of the newly added youtube query policy ***without*** further guidance, backtesting or content analysis. This can be improved by adding a content triage based on Clip2 and transcript analysis. 



https://github.com/su77ungr/FreeShortGPT/assets/69374354/4b561ba1-008a-4b91-b97b-eb14ec37f74a



deprecated_demo shows the accuracy of Google's YouTube v3, you can find it here: https://vimeo.com/851101834?share=copy.

*Disclaimer: This repo relies on paid OpenAI access to work - this has been resolved by implementing LlamaCpp and therefore the capability to use a locally hosted LLM instead. Though communication with the main repo's RayVentura stalled. So I see no reason to release it. The Files for the image contest can be submitted to lyrical(at)skiff.com (Vanilla SDXL1.0 without LoRAs) 
