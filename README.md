# gas-webpagetest

~~[Google_Apps_Script_と_Data_Studio_でパフォーマンスモニタリング](https://scrapbox.io/uknmr/Google_Apps_Script_と_Data_Studio_でパフォーマンスモニタリング) で書いたコードです。~~  
TypeScript 化しました。

## つかいかた

[clasp](https://github.com/google/clasp) をつかっています。

1. `.clasp.json` をつくります。

    ```json
    {
      "scriptId": "<script_id>",
      "projectId": "<project_id>",
      "rootDir": "dist"
    }
    ```

1. `.env` に [WebPagetest API Key](https://www.webpagetest.org/getkey.php) と対象 URI を定義します。

    ```.env
    WEBPAGETEST_API_KEY=<webpagetest_api_key>
    RUN_TEST_URL=https://example.jp/
    ```

1. スクリプトエディタから `runTest` と `getTestResults` を呼び出すトリガーを設定します。

## 参考
- [DataStudioとGASでWebPagetestの計測結果をグラフ化する | mediba Creator × Engineer Blog](http://ceblog.mediba.jp/post/154874126622/datastudio%E3%81%A8gas%E3%81%A7webpagetest%E3%81%AE%E8%A8%88%E6%B8%AC%E7%B5%90%E6%9E%9C%E3%82%92%E3%82%B0%E3%83%A9%E3%83%95%E5%8C%96%E3%81%99%E3%82%8B)
