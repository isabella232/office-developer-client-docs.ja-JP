---
title: エントリの識別子を構築します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bc2a9116-948e-4da3-96b8-26d73bcd63c4
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 1d38c0ac7ddbd24123dd51d7315644f3ad786d15
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799807"
---
# <a name="constructing-entry-identifiers"></a><span data-ttu-id="e33b3-103">エントリの識別子を構築します。</span><span class="sxs-lookup"><span data-stu-id="e33b3-103">Constructing Entry Identifiers</span></span>

  
  
<span data-ttu-id="e33b3-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e33b3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e33b3-105">エントリ id は、[エントリ ID](entryid.md)の構造で構成されます。</span><span class="sxs-lookup"><span data-stu-id="e33b3-105">Entry identifiers are constructed with the [ENTRYID](entryid.md) structure.</span></span> <span data-ttu-id="e33b3-106">**エントリ ID**の構造は、エントリ id と、実際のエントリの識別子の属性を記述するフラグで構成されます。</span><span class="sxs-lookup"><span data-stu-id="e33b3-106">The **ENTRYID** structure is composed of a flag that describes the attributes of the entry identifier and the actual entry identifier.</span></span> 
  
## <a name="entryid-structure"></a><span data-ttu-id="e33b3-107">エントリ ID の構造</span><span class="sxs-lookup"><span data-stu-id="e33b3-107">ENTRYID Structure</span></span>

<span data-ttu-id="e33b3-108">**エントリ ID**の構造体の定義は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="e33b3-108">The **ENTRYID** structure is defined as follows:</span></span> 
  
```cpp
typedef struct
{
    BYTE        abFlags[4];
    BYTE        ab[MAPI_DIM];
}  ENTRYID, FAR *LPENTRYID;
 
```

<span data-ttu-id="e33b3-109">MAPI_DIM は、MapiDefs.h ヘッダー ファイルで定義されている定数です。</span><span class="sxs-lookup"><span data-stu-id="e33b3-109">MAPI_DIM is a constant that is defined in the MapiDefs.h header file.</span></span> 
  
<span data-ttu-id="e33b3-110">4 バイトの**abFlags**メンバーの最初のバイトは種類を説明のエントリ id を使用し、次の値を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="e33b3-110">The first byte of the 4-byte **abFlags** member describes the type and use of the entry identifier and can have the following values:</span></span> 
  
- <span data-ttu-id="e33b3-111">MAPI_NOTRECI-エントリの識別子を示します、メッセージの受信者として使用できません。</span><span class="sxs-lookup"><span data-stu-id="e33b3-111">MAPI_NOTRECI — Indicates the entry identifier cannot be used as a recipient on a message.</span></span>
    
- <span data-ttu-id="e33b3-112">MAPI_NOTRESERVED-エントリ id を他のユーザーがアクセスできないことを示します。</span><span class="sxs-lookup"><span data-stu-id="e33b3-112">MAPI_NOTRESERVED — Indicates that other users cannot access the entry identifier.</span></span>
    
- <span data-ttu-id="e33b3-113">MAPI_NOW-別のタイミングでのエントリ id を使用できないということを示します。</span><span class="sxs-lookup"><span data-stu-id="e33b3-113">MAPI_NOW — Indicates that the entry identifier cannot be used at other times.</span></span>
    
- <span data-ttu-id="e33b3-114">MAPI_SHORTTERM-短期的なエントリの識別子であることを示します。</span><span class="sxs-lookup"><span data-stu-id="e33b3-114">MAPI_SHORTTERM — Indicates that the entry identifier is short-term.</span></span> <span data-ttu-id="e33b3-115">エントリの識別子の他の使用が許可されていない限り、このバイトで他のすべての値を設定しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="e33b3-115">All other values in this byte must be set unless other uses of the entry identifier are allowed.</span></span>
    
- <span data-ttu-id="e33b3-116">MAPI_THISSESSION-他のセッションのエントリ id を使用できないということを示します。</span><span class="sxs-lookup"><span data-stu-id="e33b3-116">MAPI_THISSESSION — Indicates that the entry identifier cannot be used on other sessions.</span></span>
    
- <span data-ttu-id="e33b3-117">MAPI_NOTRESERVED-その他のオブジェクトのエントリ id が他のサービス プロバイダーによって使用できることをことを示します。</span><span class="sxs-lookup"><span data-stu-id="e33b3-117">MAPI_NOTRESERVED — Indicates that the entry identifier can be used by other service providers for other objects.</span></span>
    
<span data-ttu-id="e33b3-118">アドレス帳、メッセージ ストア プロバイダーによって作成されたエントリの識別子の**ab**のメンバーは 2 つの要素で構成します。 オブジェクトを識別する、サービス ・ プロバイダー、および 1 つを識別する 16 バイトの[MAPIUID](mapiuid.md)構造体です。</span><span class="sxs-lookup"><span data-stu-id="e33b3-118">The **ab** member of entry identifiers that is created by address book and message store providers is composed of two pieces: a 16-byte [MAPIUID](mapiuid.md) structure that identifies the service provider, and a piece to identify the object.</span></span> <span data-ttu-id="e33b3-119">**MAPIUID**は、グローバルに一意の識別子または GUID を格納する構造体です。</span><span class="sxs-lookup"><span data-stu-id="e33b3-119">**MAPIUID** is a structure that contains a globally unique identifier, or GUID.</span></span> <span data-ttu-id="e33b3-120">GUID は、Microsoft Visual Studio の *[GUID の作成*を使用して作成することができるバイト オーダーに依存しない識別子を \* ツールです。</span><span class="sxs-lookup"><span data-stu-id="e33b3-120">A GUID is a byte-order-independent identifier that can be created by using the Microsoft Visual Studio*Create GUID*\* tool.</span></span> 
  
<span data-ttu-id="e33b3-121">サービス プロバイダーは、 [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)メソッドの呼び出しでのログオン プロセス中に、MAPI との**MAPIUID**構造体を登録します。</span><span class="sxs-lookup"><span data-stu-id="e33b3-121">A service provider registers its **MAPIUID** structure with MAPI during the logon process in a call to the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method.</span></span> <span data-ttu-id="e33b3-122">クライアントがオブジェクトへのアクセス、 **OpenEntry**メソッドを呼び出すと、MAPI はサービス プロバイダーは、そのアクセスを提供できるかを決定するのに**MAPIUID**構造体を使用します。</span><span class="sxs-lookup"><span data-stu-id="e33b3-122">When a client calls an **OpenEntry** method to access an object, MAPI uses the **MAPIUID** structure to determine which service provider can provide that access.</span></span> <span data-ttu-id="e33b3-123">サービス プロバイダーは、その DLL のすべてのバージョンの**MAPIUID**と同じ構造を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e33b3-123">Service providers should use the same **MAPIUID** structure for all versions of their DLL.</span></span> <span data-ttu-id="e33b3-124">これにより、新しいバージョンのクライアントが応答メッセージを送信し、以前のバージョンで保存します。</span><span class="sxs-lookup"><span data-stu-id="e33b3-124">This enables clients with the newer version to respond to messages sent and saved with the older version.</span></span> 
  
<span data-ttu-id="e33b3-125">16 バイトの**MAPIUID**の後の**ab**のメンバーの残りの部分には、特定のオブジェクトを識別するためのサービス ・ プロバイダーに固有のバイナリ データが含まれています。</span><span class="sxs-lookup"><span data-stu-id="e33b3-125">The rest of the **ab** member after the 16-byte **MAPIUID** contains service-provider-specific binary data for identifying particular objects.</span></span> <span data-ttu-id="e33b3-126">エントリ id のこの部分のサイズは固定されていません。</span><span class="sxs-lookup"><span data-stu-id="e33b3-126">There is no fixed size for this portion of the entry identifier.</span></span> <span data-ttu-id="e33b3-127">理由内の任意のサイズを指定できます。</span><span class="sxs-lookup"><span data-stu-id="e33b3-127">It can be any size, within reason.</span></span> <span data-ttu-id="e33b3-128">通常、サービス プロバイダーには、そのエントリ id のこの部分の次の情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="e33b3-128">A service provider typically includes the following information in this part of its entry identifiers:</span></span> 
  
- <span data-ttu-id="e33b3-129">バージョン情報、バージョンのエントリ id の形式を変更するのにはサービス ・ プロバイダーの一般的なので、バージョン情報を格納するによって、任意のエントリの識別子を判別する方法をすぐに確認します。</span><span class="sxs-lookup"><span data-stu-id="e33b3-129">Version information — Because it is common for a service provider to change the format of its entry identifiers from version to version, storing version information makes it possible to quickly determine how to decipher any entry identifier.</span></span>
    
- <span data-ttu-id="e33b3-130">場所情報-場所の情報は、データ サービス プロバイダーのエントリの識別子によって表されるオブジェクトを検索する方法を示すインジケーターを提供します。</span><span class="sxs-lookup"><span data-stu-id="e33b3-130">Location information — Location information is data that gives a service provider an indicator of how to locate the object represented by the entry identifier.</span></span> <span data-ttu-id="e33b3-131">たとえば、サービス プロバイダーは、ディスク オブジェクトが格納されたデータ ファイル内の最後の場所のオフセットを格納できます。</span><span class="sxs-lookup"><span data-stu-id="e33b3-131">For example, a service provider can store the disk offset for the last place in a data file that the object was stored.</span></span> <span data-ttu-id="e33b3-132">この種の情報は、時間の経過とともに変更できます、ために、サービス プロバイダーは、それらのエントリの識別子でオブジェクトを検索するため複数の方法を提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e33b3-132">Because this type of information can change over time, service providers should provide multiple ways for locating objects in their entry identifiers.</span></span>
    
<span data-ttu-id="e33b3-133">サービス プロバイダーは、それらのエントリの識別子をリサイクルできるが、この方法は避けてください。</span><span class="sxs-lookup"><span data-stu-id="e33b3-133">Although service providers can recycle their entry identifiers, they should avoid this practice.</span></span> <span data-ttu-id="e33b3-134">エントリ識別子を再利用する必要がある場合、サービス プロバイダーは最初の使用は、可能な限り再利用するまでに経過するまでの時間をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e33b3-134">If it is necessary to reuse an entry identifier, service providers should make the time period that elapses between the initial use and the reuse as long as possible.</span></span> <span data-ttu-id="e33b3-135">同じ種類の別のオブジェクトのエントリ id を再割り当てする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e33b3-135">Also, the entry identifier should be reassigned to another object of the same type.</span></span> <span data-ttu-id="e33b3-136">特定のエントリの識別子をメッセージから開始し、フォルダーに関連付けられている必要がありますできません。</span><span class="sxs-lookup"><span data-stu-id="e33b3-136">That is, a particular entry identifier should not be associated first with a message and then with a folder.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e33b3-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="e33b3-137">See also</span></span>



[<span data-ttu-id="e33b3-138">MAPI エントリの識別子</span><span class="sxs-lookup"><span data-stu-id="e33b3-138">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

