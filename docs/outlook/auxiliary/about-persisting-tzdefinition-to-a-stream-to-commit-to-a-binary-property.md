---
title: バイナリ プロパティにコミットするためにストリームに TZDEFINITION を保持することについて
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 0dec535d-d48f-39a5-97d5-0bd109134b3b
description: タイム ゾーン プロパティ、PidLidAppointmentTimeZoneDefinitionEndDisplay、PidLidAppointmentTimeZoneDefinitionRecur、および PidLidAppointmentTimeZoneDefinitionStartDisplay はバイナリ名前付きプロパティであり、それぞれが TZDEFINITION 構造体の永続化された形式にマップされるストリームを含みます。
ms.openlocfilehash: 6925068faf9e4e4e700ea8d2aae2fd25dc98cdb1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592838"
---
# <a name="about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property"></a>バイナリ プロパティにコミットするためにストリームに TZDEFINITION を保持することについて

タイム ゾーン プロパティ[、PidLidAppointmentTimeZoneDefinitionEndDisplay、PidLidAppointmentTimeZoneDefinitionRecur、](https://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx)および[PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx)はバイナリ名前付きプロパティであり、それぞれが[TZDEFINITION](tzdefinition.md)構造体の永続化された形式にマップされるストリームを含みます。 [](https://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx) 
  
このトピックでは **、TZDEFINITION** をストリームに永続化して 3 つのバイナリ プロパティの 1 つをコミットするときに使用できる、少しエンディアン形式について説明します。 パーサーで同じエンディアン形式を使用して、これらのプロパティの 1 つから取得したストリーム値を解釈します。 
  
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

メジャー バージョン番号を使用して、大きな変更を行います。 メジャー バージョン番号に慣れていないクライアントは、プロパティがそこにない場合と同様に処理する必要があります。 構造を記述するクライアントは、定数を指定する **必要TZ_BIN_VERSION_MAJOR。** 
  
マイナー バージョン番号は、機能拡張に使用されます。 マイナー バージョン番号に慣れていないクライアントは、理解しているデータを読み取り、各ルールまたはストリーム全体に追加される可能性のあるデータをスキップする必要があります。 構造を記述するクライアントは、定数を指定する **必要TZ_BIN_VERSION_MINOR。** 
  
パーサーがヘッダーのメジャー バージョンを理解していない場合は、構造の残りの部分を読み取り、データが不足している場合と同様に動作する必要があります。 パーサーがヘッダーのマイナー バージョンを理解していない場合は **、cbHeader** を使用して、理解していない部分を無視し、理解しているストリームの部分を読み取る前に進む必要があります。 
  
**wFlags の値は** 常 **に** TZDEFINITION_FLAG_VALID_KEYNAME。 キー名の最大サイズは、MAX_PATH **です。** 
  
パーサーがメジャー バージョンのルールを認識しない場合、クライアントはルールを無視し **、cbRule** を使用して次のルールに進む必要があります。 パーサーがルールのマイナー バージョンを認識しない場合、クライアントは、理解しているルールの一部のみを解析する必要があります。 
  
**TZDEFINITION** 構造体をストリームに永続化する場合、パーサーは理解できない情報を書き込もうとしません。 
  
ルールの最大数は 1024 です。
  
[TZREG 構造は](tzreg.md)、単独で永続化する場合とは異なる方法で保持されます。そのため、同じコードを使用して解析することはできません。 
  
## <a name="see-also"></a>関連項目

- [(Outlook エクスポート Api) 定数](constants-outlook-exported-apis.md)
- [バイナリ プロパティからのストリームを解析し、TZDEFINITION 構造体を読み取る](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [予定からタイム ゾーンのプロパティを読み取る](how-to-read-time-zone-properties-from-an-appointment.md)

