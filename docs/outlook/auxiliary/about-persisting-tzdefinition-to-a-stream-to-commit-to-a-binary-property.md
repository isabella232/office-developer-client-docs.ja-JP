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
# <a name="about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property"></a><span data-ttu-id="9b617-103">バイナリ プロパティにコミットするためにストリームに TZDEFINITION を保持することについて</span><span class="sxs-lookup"><span data-stu-id="9b617-103">About persisting TZDEFINITION to a stream to commit to a binary property</span></span>

<span data-ttu-id="9b617-104">タイムゾーンのプロパティ、 [PidLidAppointmentTimeZoneDefinitionEndDisplay](https://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx)、 [PidLidAppointmentTimeZoneDefinitionRecur](https://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx)、および[PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx)は、バイナリという名前のプロパティで、各[TZDEFINITION](tzdefinition.md)構造の永続化された形式にマップするストリームを格納します。</span><span class="sxs-lookup"><span data-stu-id="9b617-104">The time zone properties, [PidLidAppointmentTimeZoneDefinitionEndDisplay](https://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx), [PidLidAppointmentTimeZoneDefinitionRecur](https://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx), and [PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx) are binary named properties, each of which contains a stream that maps to the persisted format of a [TZDEFINITION](tzdefinition.md) structure.</span></span> 
  
<span data-ttu-id="9b617-105">このトピックでは、 **TZDEFINITION**を stream に永続化して、3つのバイナリプロパティのいずれかにコミットするときに使用できるリトルエンディアン形式について説明します。</span><span class="sxs-lookup"><span data-stu-id="9b617-105">This topic describes a little endian format that can be used when persisting **TZDEFINITION** to a stream to commit to one of three binary properties.</span></span> <span data-ttu-id="9b617-106">これらのプロパティのいずれかから取得したストリーム値を解釈するには、パーサーで同じエンディアン形式を使用します。</span><span class="sxs-lookup"><span data-stu-id="9b617-106">Use the same endian format in a parser to interpret a stream value obtained from one of these properties.</span></span> 
  
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

<span data-ttu-id="9b617-107">メジャーバージョン番号は、互換性に影響する変更を行うために使用されます。</span><span class="sxs-lookup"><span data-stu-id="9b617-107">The major version number is used to make a breaking change.</span></span> <span data-ttu-id="9b617-108">メジャーバージョン番号に不慣れなクライアントでは、プロパティが存在しない場合と同様に処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b617-108">Clients that are unfamiliar with the major version number should treat the property as if it is not there.</span></span> <span data-ttu-id="9b617-109">構造を書き込むクライアントは、定数**TZ_BIN_VERSION_MAJOR**を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b617-109">Clients writing the structure should specify the constant **TZ_BIN_VERSION_MAJOR**.</span></span> 
  
<span data-ttu-id="9b617-110">マイナーバージョン番号は、拡張性のために使用されます。</span><span class="sxs-lookup"><span data-stu-id="9b617-110">The minor version number is used for extensibility.</span></span> <span data-ttu-id="9b617-111">マイナーバージョン番号に不慣れなクライアントは、自分が理解しているデータを読み取って、各ルールまたはストリーム全体に追加される可能性のあるデータをスキップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b617-111">Clients that are unfamiliar with the minor version number should read the data that they understand, and skip over the data that might be appended to each rule or to the overall stream.</span></span> <span data-ttu-id="9b617-112">構造を書き込むクライアントは、定数**TZ_BIN_VERSION_MINOR**を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b617-112">Clients writing the structure should specify the constant **TZ_BIN_VERSION_MINOR**.</span></span> 
  
<span data-ttu-id="9b617-113">パーサーがヘッダーのメジャーバージョンを認識しない場合、その構造体の残りの部分を読み取らず、データが欠落しているかのように動作する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b617-113">If a parser does not understand the major version of the header, it should not read the rest of the structure and behave as if the data is missing.</span></span> <span data-ttu-id="9b617-114">パーサーがヘッダーのマイナーバージョンを認識しない場合は、 **cbheader**を使用して、理解していない部分を無視して、認識されるストリームの部分を読み取る必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b617-114">If a parser does not understand the minor version of the header, it should use **cbHeader** to ignore the portions that it does not understand and advance to read the portions of the stream that it understands.</span></span> 
  
<span data-ttu-id="9b617-115">**wflags**の値は常に**TZDEFINITION_FLAG_VALID_KEYNAME**です。</span><span class="sxs-lookup"><span data-stu-id="9b617-115">The value of **wFlags** is always **TZDEFINITION_FLAG_VALID_KEYNAME**.</span></span> <span data-ttu-id="9b617-116">キー名の最大サイズは**MAX_PATH**です。</span><span class="sxs-lookup"><span data-stu-id="9b617-116">The key name has a maximum size of **MAX_PATH**.</span></span> 
  
<span data-ttu-id="9b617-117">パーサーがルールのメジャーバージョンを認識しない場合は、クライアントはルールを無視し、 **cbrule**指定を使用して次のルールに進みます。</span><span class="sxs-lookup"><span data-stu-id="9b617-117">If a parser does not recognize the major version of a rule, the client should ignore the rule, and use **cbRule** to advance to the next rule.</span></span> <span data-ttu-id="9b617-118">パーサーがルールのマイナーバージョンを認識しない場合、クライアントは、ルールを認識する部分のみを解析する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b617-118">If a parser does not recognize the minor version of a rule, the client should only parse the parts of the rule that it understands.</span></span> 
  
<span data-ttu-id="9b617-119">**TZDEFINITION**構造体をストリームに永続化する場合、パーサーは、認識できない情報を書き込めないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="9b617-119">When persisting a **TZDEFINITION** structure to a stream, a parser should not try to write any information that it does not understand.</span></span> 
  
<span data-ttu-id="9b617-120">ルールの最大数は1024です。</span><span class="sxs-lookup"><span data-stu-id="9b617-120">The maximum number of rules is 1024.</span></span>
  
<span data-ttu-id="9b617-121">[TZREG](tzreg.md)構造体は単独で永続化する場合とは異なる方法で保持されるため、同じコードを使用して解析することはできません。</span><span class="sxs-lookup"><span data-stu-id="9b617-121">Note that the [TZREG](tzreg.md) structure is persisted here differently than when persisted alone, so the same code cannot be used to parse it.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9b617-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="9b617-122">See also</span></span>

- [<span data-ttu-id="9b617-123">(Outlook エクスポート Api) 定数</span><span class="sxs-lookup"><span data-stu-id="9b617-123">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)
- [<span data-ttu-id="9b617-124">バイナリ プロパティからのストリームを解析し、TZDEFINITION 構造体を読み取る</span><span class="sxs-lookup"><span data-stu-id="9b617-124">Parse a stream from a binary property to read the TZDEFINITION structure</span></span>](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [<span data-ttu-id="9b617-125">予定からタイム ゾーンのプロパティを読み取る</span><span class="sxs-lookup"><span data-stu-id="9b617-125">Read time zone properties from an appointment</span></span>](how-to-read-time-zone-properties-from-an-appointment.md)

