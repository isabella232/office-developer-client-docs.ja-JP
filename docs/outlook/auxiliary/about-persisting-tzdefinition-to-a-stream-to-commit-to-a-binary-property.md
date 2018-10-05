---
title: バイナリ プロパティにコミットするためにストリームに TZDEFINITION を保持することについて
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 0dec535d-d48f-39a5-97d5-0bd109134b3b
description: タイム ゾーンのプロパティ、PidLidAppointmentTimeZoneDefinitionEndDisplay、PidLidAppointmentTimeZoneDefinitionRecur、および PidLidAppointmentTimeZoneDefinitionStartDisplay はバイナリに対応するストリームを含む、プロパティの名前、TZDEFINITION 構造体の永続化された形式です。
ms.openlocfilehash: f94b751a55aa852c962eebe5d46968e9e622e315
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398620"
---
# <a name="about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property"></a><span data-ttu-id="77a26-103">バイナリ プロパティにコミットするためにストリームに TZDEFINITION を保持することについて</span><span class="sxs-lookup"><span data-stu-id="77a26-103">About persisting TZDEFINITION to a stream to commit to a binary property</span></span>

<span data-ttu-id="77a26-104">タイム ゾーンのプロパティ、 [PidLidAppointmentTimeZoneDefinitionEndDisplay](https://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx)、 [PidLidAppointmentTimeZoneDefinitionRecur](https://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx)、および[PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx)はバイナリのプロパティを名前付きの[TZDEFINITION](tzdefinition.md)構造体の保存形式に対応するストリームが含まれています。</span><span class="sxs-lookup"><span data-stu-id="77a26-104">The time zone properties, [PidLidAppointmentTimeZoneDefinitionEndDisplay](https://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx), [PidLidAppointmentTimeZoneDefinitionRecur](https://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx), and [PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx) are binary named properties, each of which contains a stream that maps to the persisted format of a [TZDEFINITION](tzdefinition.md) structure.</span></span> 
  
<span data-ttu-id="77a26-105">このトピックでは、次の 3 つのバイナリ プロパティのいずれかにコミットする**TZDEFINITION**をストリームに保存する場合に使用できる、リトル エンディアン形式について説明します。</span><span class="sxs-lookup"><span data-stu-id="77a26-105">This topic describes a little endian format that can be used when persisting **TZDEFINITION** to a stream to commit to one of three binary properties.</span></span> <span data-ttu-id="77a26-106">これらのプロパティのいずれかから取得したストリームの値を解釈するためにパーサーで同じのエンディアンの形式を使用します。</span><span class="sxs-lookup"><span data-stu-id="77a26-106">Use the same endian format in a parser to interpret a stream value obtained from one of these properties.</span></span> 
  
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

<span data-ttu-id="77a26-107">メジャー バージョン番号を使用して、変更、互換性に影響を確認します。</span><span class="sxs-lookup"><span data-stu-id="77a26-107">The major version number is used to make a breaking change.</span></span> <span data-ttu-id="77a26-108">メジャー バージョン番号に慣れていないするクライアントが存在しないかのようにプロパティを扱う必要があります。</span><span class="sxs-lookup"><span data-stu-id="77a26-108">Clients that are unfamiliar with the major version number should treat the property as if it is not there.</span></span> <span data-ttu-id="77a26-109">クライアントの構造を記述するには、定数**TZ_BIN_VERSION_MAJOR**を指定してください。</span><span class="sxs-lookup"><span data-stu-id="77a26-109">Clients writing the structure should specify the constant **TZ_BIN_VERSION_MAJOR**.</span></span> 
  
<span data-ttu-id="77a26-110">マイナー バージョン番号は、機能拡張に使用されます。</span><span class="sxs-lookup"><span data-stu-id="77a26-110">The minor version number is used for extensibility.</span></span> <span data-ttu-id="77a26-111">マイナー バージョン番号に慣れていないするクライアントは、データを理解し、ルールごとに、または全体のストリームに追加することがありますデータはスキップされるはずです。</span><span class="sxs-lookup"><span data-stu-id="77a26-111">Clients that are unfamiliar with the minor version number should read the data that they understand, and skip over the data that might be appended to each rule or to the overall stream.</span></span> <span data-ttu-id="77a26-112">クライアントの構造を記述するには、定数**TZ_BIN_VERSION_MINOR**を指定してください。</span><span class="sxs-lookup"><span data-stu-id="77a26-112">Clients writing the structure should specify the constant **TZ_BIN_VERSION_MINOR**.</span></span> 
  
<span data-ttu-id="77a26-113">パーサーが、ヘッダーのメジャー バージョンを認識しない場合する必要があります構造体の残りの部分を読んでされず、データが不足しているように動作します。</span><span class="sxs-lookup"><span data-stu-id="77a26-113">If a parser does not understand the major version of the header, it should not read the rest of the structure and behave as if the data is missing.</span></span> <span data-ttu-id="77a26-114">パーサーが、ヘッダーのマイナー バージョンを認識しない場合は、それに対応していない部分と理解しているストリームの一部を読み取るための高度を無視するように**cbHeader**を使用してください。</span><span class="sxs-lookup"><span data-stu-id="77a26-114">If a parser does not understand the minor version of the header, it should use **cbHeader** to ignore the portions that it does not understand and advance to read the portions of the stream that it understands.</span></span> 
  
<span data-ttu-id="77a26-115">**WFlags**の値は、常に**TZDEFINITION_FLAG_VALID_KEYNAME**です。</span><span class="sxs-lookup"><span data-stu-id="77a26-115">The value of **wFlags** is always **TZDEFINITION_FLAG_VALID_KEYNAME**.</span></span> <span data-ttu-id="77a26-116">キー名は、 **MAX_PATH**の最大サイズです。</span><span class="sxs-lookup"><span data-stu-id="77a26-116">The key name has a maximum size of **MAX_PATH**.</span></span> 
  
<span data-ttu-id="77a26-117">ルールのメジャー バージョンが、パーサーで認識されない場合、ルールを無視するクライアント側で確認し、 **cbRule**を使用して、次のルールに移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="77a26-117">If a parser does not recognize the major version of a rule, the client should ignore the rule, and use **cbRule** to advance to the next rule.</span></span> <span data-ttu-id="77a26-118">パーサーは、ルールのマイナー バージョンを認識できない場合は、クライアントする必要があります理解しているルールの構成要素を解析してのみ。</span><span class="sxs-lookup"><span data-stu-id="77a26-118">If a parser does not recognize the minor version of a rule, the client should only parse the parts of the rule that it understands.</span></span> 
  
<span data-ttu-id="77a26-119">ストリームに**TZDEFINITION**構造体を保持する場合、パーサーくださいそれに対応していないすべての情報を記述します。</span><span class="sxs-lookup"><span data-stu-id="77a26-119">When persisting a **TZDEFINITION** structure to a stream, a parser should not try to write any information that it does not understand.</span></span> 
  
<span data-ttu-id="77a26-120">ルールの最大数は、1024 です。</span><span class="sxs-lookup"><span data-stu-id="77a26-120">The maximum number of rules is 1024.</span></span>
  
<span data-ttu-id="77a26-121">[TZREG](tzreg.md)構造体が保持されているこことは異なる、単独で永続化すると、同じコードは使用できませんそれを解析するよりも注意してください。</span><span class="sxs-lookup"><span data-stu-id="77a26-121">Note that the [TZREG](tzreg.md) structure is persisted here differently than when persisted alone, so the same code cannot be used to parse it.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="77a26-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="77a26-122">See also</span></span>

- [<span data-ttu-id="77a26-123">(Outlook エクスポート Api) 定数</span><span class="sxs-lookup"><span data-stu-id="77a26-123">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)
- [<span data-ttu-id="77a26-124">バイナリ プロパティからのストリームを解析し、TZDEFINITION 構造体を読み取る</span><span class="sxs-lookup"><span data-stu-id="77a26-124">Parse a stream from a binary property to read the TZDEFINITION structure</span></span>](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [<span data-ttu-id="77a26-125">予定からタイム ゾーンのプロパティを読み取る</span><span class="sxs-lookup"><span data-stu-id="77a26-125">Read time zone properties from an appointment</span></span>](how-to-read-time-zone-properties-from-an-appointment.md)

