---
title: バイナリ プロパティをコミットするためのストリームに永続化する TZDEFINITION について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 0dec535d-d48f-39a5-97d5-0bd109134b3b
description: タイム ゾーンのプロパティ、PidLidAppointmentTimeZoneDefinitionEndDisplay、PidLidAppointmentTimeZoneDefinitionRecur、および PidLidAppointmentTimeZoneDefinitionStartDisplay はバイナリに対応するストリームを含む、プロパティの名前、TZDEFINITION 構造体の永続化された形式です。
ms.openlocfilehash: 8e00c7203e2a0adfdf9ff3e6dadff6485c8b5111
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799294"
---
# <a name="about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property"></a>バイナリ プロパティをコミットするためのストリームに永続化する TZDEFINITION について

タイム ゾーンのプロパティ、 [PidLidAppointmentTimeZoneDefinitionEndDisplay](http://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx)、 [PidLidAppointmentTimeZoneDefinitionRecur](http://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx)、および[PidLidAppointmentTimeZoneDefinitionStartDisplay](http://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx)はバイナリのプロパティを名前付きの[TZDEFINITION](tzdefinition.md)構造体の保存形式に対応するストリームが含まれています。 
  
このトピックでは、次の 3 つのバイナリ プロパティのいずれかにコミットする**TZDEFINITION**をストリームに保存する場合に使用できる、リトル エンディアン形式について説明します。 これらのプロパティのいずれかから取得したストリームの値を解釈するためにパーサーで同じのエンディアンの形式を使用します。 
  
```cpp
BYTE  bMajorVersion;    // breaking change
BYTE  bMinorVersion;    // extensibility
WORD  cbHeader;         // size of following data until TZREG sub structure
WORD  wFlags;
if (TZDEFINITION_FLAG_VALID_GUID)
   GUID  guid;                // guid
if (TZDEFINITION_FLAG_VALID_KEYNAME)     
    WORD   cchKeyName;        // does not include null char
    WCHAR  rgchKeyName;       // not null terminated
    WORD  cRules;             // number of rules
// for each rule
   BYTE        bMajorVersion;         // breaking change
   BYTE        bMinorVersion;         // extensibility
   WORD        cbRule;                // size of following data
   WORD        wFlags;                // flags
   SYSTEMTIME  stStart;               // GMT when this rule starts
// Following are the fields of the TZREG sub structure
   long        lBias;                // offset from GMT
   long        lStandardBias;        // offset from bias during standard time
   long        lDaylightBias;        // offset from bias during daylight time
   SYSTEMTIME  stStandardDate;       // time to switch to standard time
   SYSTEMTIME  stDaylightDate;       // time to switch to daylight time
```

メジャー バージョン番号を使用して、変更、互換性に影響を確認します。 メジャー バージョン番号に慣れていないするクライアントが存在しないかのようにプロパティを扱う必要があります。 クライアントの構造を記述するには、定数**TZ_BIN_VERSION_MAJOR**を指定してください。 
  
マイナー バージョン番号は、機能拡張に使用されます。 マイナー バージョン番号に慣れていないするクライアントは、データを理解し、ルールごとに、または全体のストリームに追加することがありますデータはスキップされるはずです。 クライアントの構造を記述するには、定数**TZ_BIN_VERSION_MINOR**を指定してください。 
  
パーサーが、ヘッダーのメジャー バージョンを認識しない場合する必要があります構造体の残りの部分を読んでされず、データが不足しているように動作します。 パーサーが、ヘッダーのマイナー バージョンを認識しない場合は、それに対応していない部分と理解しているストリームの一部を読み取るための高度を無視するように**cbHeader**を使用してください。 
  
**WFlags**の値は、常に**TZDEFINITION_FLAG_VALID_KEYNAME**です。 キー名は、 **MAX_PATH**の最大サイズです。 
  
ルールのメジャー バージョンが、パーサーで認識されない場合、ルールを無視するクライアント側で確認し、 **cbRule**を使用して、次のルールに移動する必要があります。 パーサーは、ルールのマイナー バージョンを認識できない場合は、クライアントする必要があります理解しているルールの構成要素を解析してのみ。 
  
ストリームに**TZDEFINITION**構造体を保持する場合、パーサーくださいそれに対応していないすべての情報を記述します。 
  
ルールの最大数は、1024 です。
  
[TZREG](tzreg.md)構造体が保持されているこことは異なる、単独で永続化すると、同じコードは使用できませんそれを解析するよりも注意してください。 
  
## <a name="see-also"></a>関連項目

- [(Outlook エクスポート Api) 定数](constants-outlook-exported-apis.md)
- [TZDEFINITION 構造体を読み取るためのバイナリのプロパティからのストリームを解析します。](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [予定からタイム ゾーンのプロパティを読み取る](how-to-read-time-zone-properties-from-an-appointment.md)

