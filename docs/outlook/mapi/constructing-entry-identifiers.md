---
title: エントリ識別子の作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bc2a9116-948e-4da3-96b8-26d73bcd63c4
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8d48c2584fa5b7e862102e401ea8165821607f77
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427949"
---
# <a name="constructing-entry-identifiers"></a><span data-ttu-id="b1075-103">エントリ識別子の作成</span><span class="sxs-lookup"><span data-stu-id="b1075-103">Constructing Entry Identifiers</span></span>

  
  
<span data-ttu-id="b1075-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1075-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1075-105">エントリ識別子は [ENTRYID 構造で構築](entryid.md) されます。</span><span class="sxs-lookup"><span data-stu-id="b1075-105">Entry identifiers are constructed with the [ENTRYID](entryid.md) structure.</span></span> <span data-ttu-id="b1075-106">**ENTRYID 構造体は**、エントリ識別子の属性と実際のエントリ識別子を記述するフラグで構成されます。</span><span class="sxs-lookup"><span data-stu-id="b1075-106">The **ENTRYID** structure is composed of a flag that describes the attributes of the entry identifier and the actual entry identifier.</span></span> 
  
## <a name="entryid-structure"></a><span data-ttu-id="b1075-107">ENTRYID 構造</span><span class="sxs-lookup"><span data-stu-id="b1075-107">ENTRYID Structure</span></span>

<span data-ttu-id="b1075-108">**ENTRYID 構造は** 次のように定義されます。</span><span class="sxs-lookup"><span data-stu-id="b1075-108">The **ENTRYID** structure is defined as follows:</span></span> 
  
```cpp
typedef struct
{
    BYTE        abFlags[4];
    BYTE        ab[MAPI_DIM];
}  ENTRYID, FAR *LPENTRYID;
 
```

<span data-ttu-id="b1075-109">MAPI_DIMは、MapiDefs.h ヘッダー ファイルで定義されている定数です。</span><span class="sxs-lookup"><span data-stu-id="b1075-109">MAPI_DIM is a constant that is defined in the MapiDefs.h header file.</span></span> 
  
<span data-ttu-id="b1075-110">4 バイトの **abFlags** メンバーの最初のバイトは、エントリ識別子の種類と使用について説明し、次の値を持つ場合があります。</span><span class="sxs-lookup"><span data-stu-id="b1075-110">The first byte of the 4-byte **abFlags** member describes the type and use of the entry identifier and can have the following values:</span></span> 
  
- <span data-ttu-id="b1075-111">MAPI_NOTRECI — メッセージの受信者としてエントリ識別子を使用できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="b1075-111">MAPI_NOTRECI — Indicates the entry identifier cannot be used as a recipient on a message.</span></span>
    
- <span data-ttu-id="b1075-112">MAPI_NOTRESERVED — 他のユーザーがエントリ識別子にアクセスできないことを示します。</span><span class="sxs-lookup"><span data-stu-id="b1075-112">MAPI_NOTRESERVED — Indicates that other users cannot access the entry identifier.</span></span>
    
- <span data-ttu-id="b1075-113">MAPI_NOW — エントリ識別子を他の時間に使用できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="b1075-113">MAPI_NOW — Indicates that the entry identifier cannot be used at other times.</span></span>
    
- <span data-ttu-id="b1075-114">MAPI_SHORTTERM — エントリ識別子が短期的な値を示します。</span><span class="sxs-lookup"><span data-stu-id="b1075-114">MAPI_SHORTTERM — Indicates that the entry identifier is short-term.</span></span> <span data-ttu-id="b1075-115">エントリ識別子の他の使用が許可されていない限り、このバイト内の他のすべての値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1075-115">All other values in this byte must be set unless other uses of the entry identifier are allowed.</span></span>
    
- <span data-ttu-id="b1075-116">MAPI_THISSESSION — エントリ識別子を他のセッションで使用できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="b1075-116">MAPI_THISSESSION — Indicates that the entry identifier cannot be used on other sessions.</span></span>
    
- <span data-ttu-id="b1075-117">MAPI_NOTRESERVED — エントリ識別子を他のサービス プロバイダーが他のオブジェクトに使用できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b1075-117">MAPI_NOTRESERVED — Indicates that the entry identifier can be used by other service providers for other objects.</span></span>
    
<span data-ttu-id="b1075-118">アドレス帳とメッセージ ストア プロバイダーによって作成されるエントリ識別子の ab メンバーは、サービス プロバイダーを識別する 16 バイト[の MAPIUID](mapiuid.md)構造と、オブジェクトを識別する部分の 2 つの部分で構成されます。</span><span class="sxs-lookup"><span data-stu-id="b1075-118">The **ab** member of entry identifiers that is created by address book and message store providers is composed of two pieces: a 16-byte [MAPIUID](mapiuid.md) structure that identifies the service provider, and a piece to identify the object.</span></span> <span data-ttu-id="b1075-119">**MAPIUID は** 、グローバル一意識別子 (GUID) を含む構造体です。</span><span class="sxs-lookup"><span data-stu-id="b1075-119">**MAPIUID** is a structure that contains a globally unique identifier, or GUID.</span></span> <span data-ttu-id="b1075-120">GUID はバイトオーダーに依存しない識別子で、GUID の作成 \* ツールMicrosoft Visual Studio *使用* して作成できます。</span><span class="sxs-lookup"><span data-stu-id="b1075-120">A GUID is a byte-order-independent identifier that can be created by using the Microsoft Visual Studio *Create GUID*\* tool.</span></span> 
  
<span data-ttu-id="b1075-121">サービス プロバイダーは [、IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)メソッドへの呼び出しで、ログオン プロセス中に **MAPIUID** 構造を MAPI に登録します。</span><span class="sxs-lookup"><span data-stu-id="b1075-121">A service provider registers its **MAPIUID** structure with MAPI during the logon process in a call to the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method.</span></span> <span data-ttu-id="b1075-122">クライアントが **OpenEntry** メソッドを呼び出してオブジェクトにアクセスすると、MAPI は **MAPIUID** 構造を使用して、そのアクセスを提供できるサービス プロバイダーを特定します。</span><span class="sxs-lookup"><span data-stu-id="b1075-122">When a client calls an **OpenEntry** method to access an object, MAPI uses the **MAPIUID** structure to determine which service provider can provide that access.</span></span> <span data-ttu-id="b1075-123">サービス プロバイダーは、DLL のすべてのバージョンで同じ **MAPIUID** 構造を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1075-123">Service providers should use the same **MAPIUID** structure for all versions of their DLL.</span></span> <span data-ttu-id="b1075-124">これにより、新しいバージョンのクライアントは、以前のバージョンで送信および保存されたメッセージに応答できます。</span><span class="sxs-lookup"><span data-stu-id="b1075-124">This enables clients with the newer version to respond to messages sent and saved with the older version.</span></span> 
  
<span data-ttu-id="b1075-125">16 バイト **の** **MAPIUID** の後の ab メンバーの残りの部分には、特定のオブジェクトを識別するためのサービス プロバイダー固有のバイナリ データが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b1075-125">The rest of the **ab** member after the 16-byte **MAPIUID** contains service-provider-specific binary data for identifying particular objects.</span></span> <span data-ttu-id="b1075-126">エントリ識別子のこの部分に固定サイズはありません。</span><span class="sxs-lookup"><span data-stu-id="b1075-126">There is no fixed size for this portion of the entry identifier.</span></span> <span data-ttu-id="b1075-127">理由の範囲内で、任意のサイズを指定できます。</span><span class="sxs-lookup"><span data-stu-id="b1075-127">It can be any size, within reason.</span></span> <span data-ttu-id="b1075-128">サービス プロバイダーには、通常、エントリ識別子のこの部分に次の情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b1075-128">A service provider typically includes the following information in this part of its entry identifiers:</span></span> 
  
- <span data-ttu-id="b1075-129">バージョン情報 : サービス プロバイダーがエントリ識別子の形式をバージョンからバージョンに変更する場合が一般的なので、バージョン情報を保存すると、エントリ識別子を解読する方法をすばやく判断できます。</span><span class="sxs-lookup"><span data-stu-id="b1075-129">Version information — Because it is common for a service provider to change the format of its entry identifiers from version to version, storing version information makes it possible to quickly determine how to decipher any entry identifier.</span></span>
    
- <span data-ttu-id="b1075-130">位置情報 - 位置情報は、サービス プロバイダーにエントリ識別子で表されるオブジェクトを見つける方法を示す指標を提供するデータです。</span><span class="sxs-lookup"><span data-stu-id="b1075-130">Location information — Location information is data that gives a service provider an indicator of how to locate the object represented by the entry identifier.</span></span> <span data-ttu-id="b1075-131">たとえば、サービス プロバイダーは、オブジェクトが格納されたデータ ファイルの最後の場所のディスク オフセットを格納できます。</span><span class="sxs-lookup"><span data-stu-id="b1075-131">For example, a service provider can store the disk offset for the last place in a data file that the object was stored.</span></span> <span data-ttu-id="b1075-132">この種類の情報は時間の流中に変化する可能性があるため、サービス プロバイダーは、エントリ識別子内のオブジェクトを検索するための複数の方法を提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1075-132">Because this type of information can change over time, service providers should provide multiple ways for locating objects in their entry identifiers.</span></span>
    
<span data-ttu-id="b1075-133">サービス プロバイダーはエントリ識別子をリサイクルすることができますが、この方法は避ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1075-133">Although service providers can recycle their entry identifiers, they should avoid this practice.</span></span> <span data-ttu-id="b1075-134">エントリ識別子を再利用する必要がある場合、サービス プロバイダーは、最初の使用と再利用の間に経過する期間を可能な限り長くする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1075-134">If it is necessary to reuse an entry identifier, service providers should make the time period that elapses between the initial use and the reuse as long as possible.</span></span> <span data-ttu-id="b1075-135">また、エントリ識別子は、同じ種類の別のオブジェクトに再割り当てする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1075-135">Also, the entry identifier should be reassigned to another object of the same type.</span></span> <span data-ttu-id="b1075-136">つまり、特定のエントリ識別子を最初にメッセージに関連付け、次にフォルダーに関連付けない必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1075-136">That is, a particular entry identifier should not be associated first with a message and then with a folder.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b1075-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="b1075-137">See also</span></span>



[<span data-ttu-id="b1075-138">MAPI エントリ識別子</span><span class="sxs-lookup"><span data-stu-id="b1075-138">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

