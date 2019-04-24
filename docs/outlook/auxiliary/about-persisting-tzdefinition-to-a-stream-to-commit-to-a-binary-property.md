---
title: バイナリ プロパティにコミットするためにストリームに TZDEFINITION を保持することについて
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 0dec535d-d48f-39a5-97d5-0bd109134b3b
description: タイムゾーンのプロパティ、PidLidAppointmentTimeZoneDefinitionEndDisplay、PidLidAppointmentTimeZoneDefinitionRecur、および PidLidAppointmentTimeZoneDefinitionStartDisplay は、バイナリという名前のプロパティであり、それぞれに、それぞれに対応するストリームが含まれています。TZDEFINITION 構造の永続形式。
ms.openlocfilehash: f94b751a55aa852c962eebe5d46968e9e622e315
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316977"
---
# <a name="about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property"></a>バイナリ プロパティにコミットするためにストリームに TZDEFINITION を保持することについて

タイムゾーンのプロパティ、 [PidLidAppointmentTimeZoneDefinitionEndDisplay](https://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx)、 [PidLidAppointmentTimeZoneDefinitionRecur](https://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx)、および[PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx)は、バイナリという名前のプロパティで、各[TZDEFINITION](tzdefinition.md)構造の永続化された形式にマップするストリームを格納します。 
  
このトピックでは、 **TZDEFINITION**を stream に永続化して、3つのバイナリプロパティのいずれかにコミットするときに使用できるリトルエンディアン形式について説明します。 これらのプロパティのいずれかから取得したストリーム値を解釈するには、パーサーで同じエンディアン形式を使用します。 
  
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

メジャーバージョン番号は、互換性に影響する変更を行うために使用されます。 メジャーバージョン番号に不慣れなクライアントでは、プロパティが存在しない場合と同様に処理する必要があります。 構造を書き込むクライアントは、定数**TZ_BIN_VERSION_MAJOR**を指定する必要があります。 
  
マイナーバージョン番号は、拡張性のために使用されます。 マイナーバージョン番号に不慣れなクライアントは、自分が理解しているデータを読み取って、各ルールまたはストリーム全体に追加される可能性のあるデータをスキップする必要があります。 構造を書き込むクライアントは、定数**TZ_BIN_VERSION_MINOR**を指定する必要があります。 
  
パーサーがヘッダーのメジャーバージョンを認識しない場合、その構造体の残りの部分を読み取らず、データが欠落しているかのように動作する必要があります。 パーサーがヘッダーのマイナーバージョンを認識しない場合は、 **cbheader**を使用して、理解していない部分を無視して、認識されるストリームの部分を読み取る必要があります。 
  
**wflags**の値は常に**TZDEFINITION_FLAG_VALID_KEYNAME**です。 キー名の最大サイズは**MAX_PATH**です。 
  
パーサーがルールのメジャーバージョンを認識しない場合は、クライアントはルールを無視し、 **cbrule**指定を使用して次のルールに進みます。 パーサーがルールのマイナーバージョンを認識しない場合、クライアントは、ルールを認識する部分のみを解析する必要があります。 
  
**TZDEFINITION**構造体をストリームに永続化する場合、パーサーは、認識できない情報を書き込めないようにしてください。 
  
ルールの最大数は1024です。
  
[TZREG](tzreg.md)構造体は単独で永続化する場合とは異なる方法で保持されるため、同じコードを使用して解析することはできません。 
  
## <a name="see-also"></a>関連項目

- [(Outlook エクスポート Api) 定数](constants-outlook-exported-apis.md)
- [バイナリ プロパティからのストリームを解析し、TZDEFINITION 構造体を読み取る](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [予定からタイム ゾーンのプロパティを読み取る](how-to-read-time-zone-properties-from-an-appointment.md)

