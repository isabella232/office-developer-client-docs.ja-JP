---
title: バイナリ プロパティにコミットするためにストリームに TZDEFINITION を保持することについて
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 0dec535d-d48f-39a5-97d5-0bd109134b3b
description: タイム ゾーン プロパティ、PidLidAppointmentTimeZoneDefinitionEndDisplay、PidLidAppointmentTimeZoneDefinitionRecur、および PidLidAppointmentTimeZoneDefinitionStartDisplay はバイナリ名前付きプロパティであり、それぞれが TZDEFINITION 構造体の永続化された形式にマップされるストリームを含みます。
ms.openlocfilehash: f94b751a55aa852c962eebe5d46968e9e622e315
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316977"
---
# <a name="about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property"></a><span data-ttu-id="95d16-103">バイナリ プロパティにコミットするためにストリームに TZDEFINITION を保持することについて</span><span class="sxs-lookup"><span data-stu-id="95d16-103">About persisting TZDEFINITION to a stream to commit to a binary property</span></span>

<span data-ttu-id="95d16-104">タイム ゾーン プロパティ[、PidLidAppointmentTimeZoneDefinitionEndDisplay、PidLidAppointmentTimeZoneDefinitionRecur、](https://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx)および[PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx)はバイナリ名前付きプロパティであり、それぞれが[TZDEFINITION](tzdefinition.md)構造体の永続化された形式にマップされるストリームを含みます。 [](https://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="95d16-104">The time zone properties, [PidLidAppointmentTimeZoneDefinitionEndDisplay](https://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx), [PidLidAppointmentTimeZoneDefinitionRecur](https://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx), and [PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx) are binary named properties, each of which contains a stream that maps to the persisted format of a [TZDEFINITION](tzdefinition.md) structure.</span></span> 
  
<span data-ttu-id="95d16-105">このトピックでは **、TZDEFINITION** をストリームに永続化して 3 つのバイナリ プロパティの 1 つをコミットするときに使用できる、少しエンディアン形式について説明します。</span><span class="sxs-lookup"><span data-stu-id="95d16-105">This topic describes a little endian format that can be used when persisting **TZDEFINITION** to a stream to commit to one of three binary properties.</span></span> <span data-ttu-id="95d16-106">パーサーで同じエンディアン形式を使用して、これらのプロパティの 1 つから取得したストリーム値を解釈します。</span><span class="sxs-lookup"><span data-stu-id="95d16-106">Use the same endian format in a parser to interpret a stream value obtained from one of these properties.</span></span> 
  
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

<span data-ttu-id="95d16-107">メジャー バージョン番号を使用して、大きな変更を行います。</span><span class="sxs-lookup"><span data-stu-id="95d16-107">The major version number is used to make a breaking change.</span></span> <span data-ttu-id="95d16-108">メジャー バージョン番号に慣れていないクライアントは、プロパティがそこにない場合と同様に処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="95d16-108">Clients that are unfamiliar with the major version number should treat the property as if it is not there.</span></span> <span data-ttu-id="95d16-109">構造を記述するクライアントは、定数を指定する **必要TZ_BIN_VERSION_MAJOR。**</span><span class="sxs-lookup"><span data-stu-id="95d16-109">Clients writing the structure should specify the constant **TZ_BIN_VERSION_MAJOR**.</span></span> 
  
<span data-ttu-id="95d16-110">マイナー バージョン番号は、機能拡張に使用されます。</span><span class="sxs-lookup"><span data-stu-id="95d16-110">The minor version number is used for extensibility.</span></span> <span data-ttu-id="95d16-111">マイナー バージョン番号に慣れていないクライアントは、理解しているデータを読み取り、各ルールまたはストリーム全体に追加される可能性のあるデータをスキップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="95d16-111">Clients that are unfamiliar with the minor version number should read the data that they understand, and skip over the data that might be appended to each rule or to the overall stream.</span></span> <span data-ttu-id="95d16-112">構造を記述するクライアントは、定数を指定する **必要TZ_BIN_VERSION_MINOR。**</span><span class="sxs-lookup"><span data-stu-id="95d16-112">Clients writing the structure should specify the constant **TZ_BIN_VERSION_MINOR**.</span></span> 
  
<span data-ttu-id="95d16-113">パーサーがヘッダーのメジャー バージョンを理解していない場合は、構造の残りの部分を読み取り、データが不足している場合と同様に動作する必要があります。</span><span class="sxs-lookup"><span data-stu-id="95d16-113">If a parser does not understand the major version of the header, it should not read the rest of the structure and behave as if the data is missing.</span></span> <span data-ttu-id="95d16-114">パーサーがヘッダーのマイナー バージョンを理解していない場合は **、cbHeader** を使用して、理解していない部分を無視し、理解しているストリームの部分を読み取る前に進む必要があります。</span><span class="sxs-lookup"><span data-stu-id="95d16-114">If a parser does not understand the minor version of the header, it should use **cbHeader** to ignore the portions that it does not understand and advance to read the portions of the stream that it understands.</span></span> 
  
<span data-ttu-id="95d16-115">**wFlags の値は** 常 **に** TZDEFINITION_FLAG_VALID_KEYNAME。</span><span class="sxs-lookup"><span data-stu-id="95d16-115">The value of **wFlags** is always **TZDEFINITION_FLAG_VALID_KEYNAME**.</span></span> <span data-ttu-id="95d16-116">キー名の最大サイズは、MAX_PATH **です。**</span><span class="sxs-lookup"><span data-stu-id="95d16-116">The key name has a maximum size of **MAX_PATH**.</span></span> 
  
<span data-ttu-id="95d16-117">パーサーがメジャー バージョンのルールを認識しない場合、クライアントはルールを無視し **、cbRule** を使用して次のルールに進む必要があります。</span><span class="sxs-lookup"><span data-stu-id="95d16-117">If a parser does not recognize the major version of a rule, the client should ignore the rule, and use **cbRule** to advance to the next rule.</span></span> <span data-ttu-id="95d16-118">パーサーがルールのマイナー バージョンを認識しない場合、クライアントは、理解しているルールの一部のみを解析する必要があります。</span><span class="sxs-lookup"><span data-stu-id="95d16-118">If a parser does not recognize the minor version of a rule, the client should only parse the parts of the rule that it understands.</span></span> 
  
<span data-ttu-id="95d16-119">**TZDEFINITION** 構造体をストリームに永続化する場合、パーサーは理解できない情報を書き込もうとしません。</span><span class="sxs-lookup"><span data-stu-id="95d16-119">When persisting a **TZDEFINITION** structure to a stream, a parser should not try to write any information that it does not understand.</span></span> 
  
<span data-ttu-id="95d16-120">ルールの最大数は 1024 です。</span><span class="sxs-lookup"><span data-stu-id="95d16-120">The maximum number of rules is 1024.</span></span>
  
<span data-ttu-id="95d16-121">[TZREG 構造は](tzreg.md)、単独で永続化する場合とは異なる方法で保持されます。そのため、同じコードを使用して解析することはできません。</span><span class="sxs-lookup"><span data-stu-id="95d16-121">Note that the [TZREG](tzreg.md) structure is persisted here differently than when persisted alone, so the same code cannot be used to parse it.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="95d16-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="95d16-122">See also</span></span>

- [<span data-ttu-id="95d16-123">(Outlook エクスポート Api) 定数</span><span class="sxs-lookup"><span data-stu-id="95d16-123">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)
- [<span data-ttu-id="95d16-124">バイナリ プロパティからのストリームを解析し、TZDEFINITION 構造体を読み取る</span><span class="sxs-lookup"><span data-stu-id="95d16-124">Parse a stream from a binary property to read the TZDEFINITION structure</span></span>](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [<span data-ttu-id="95d16-125">予定からタイム ゾーンのプロパティを読み取る</span><span class="sxs-lookup"><span data-stu-id="95d16-125">Read time zone properties from an appointment</span></span>](how-to-read-time-zone-properties-from-an-appointment.md)

