---
title: インデックス作成のためのストア登録について
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dd2aa06a-96e8-1291-18b5-fc3c40b74e4d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 96322d12b3b7b334b5f78f81910dcf34c3fc78e1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386531"
---
# <a name="about-registering-stores-for-indexing"></a><span data-ttu-id="2130c-103">インデックス作成のためのストア登録について</span><span class="sxs-lookup"><span data-stu-id="2130c-103">About Registering Stores for Indexing</span></span>

  
  
<span data-ttu-id="2130c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2130c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2130c-105">このトピックは、Microsoft Office Outlook 2007 でクイック検索を特定します。</span><span class="sxs-lookup"><span data-stu-id="2130c-105">This topic is specific to Instant Search in Microsoft Office Outlook 2007.</span></span>
  
<span data-ttu-id="2130c-106">クイック検索では、Outlook でアイテムをすばやく検索することができます。</span><span class="sxs-lookup"><span data-stu-id="2130c-106">Instant Search lets you quickly find items in Outlook.</span></span> <span data-ttu-id="2130c-107">Windows デスクトップ サーチのコンポーネントを使用します。</span><span class="sxs-lookup"><span data-stu-id="2130c-107">It uses components of Windows Desktop Search.</span></span>
  
<span data-ttu-id="2130c-108">MAPI プロトコル ハンドラーでは、検索用のストアにインデックスを作成するための Windows レジストリをチェックします。</span><span class="sxs-lookup"><span data-stu-id="2130c-108">The MAPI Protocol Handler checks the Windows registry for stores that it should index for search purposes.</span></span> <span data-ttu-id="2130c-109">インデックスを作成するストア プロバイダーは、Windows レジストリに登録しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="2130c-109">Store providers that want to be indexed must be registered in the Windows registry.</span></span>
  
<span data-ttu-id="2130c-110">既定では、Windows デスクトップ サーチのインデックス作成を許可する Windows レジストリに、ストア プロバイダーの次の 4 種類が追加されます。</span><span class="sxs-lookup"><span data-stu-id="2130c-110">By default, Windows Desktop Search adds the following four types of store providers to the Windows registry to allow indexing:</span></span>
  
- <span data-ttu-id="2130c-111">ストアの個人用フォルダー ファイル (。PST) です。</span><span class="sxs-lookup"><span data-stu-id="2130c-111">Store for Personal Folders files (.PST).</span></span>
    
-  <span data-ttu-id="2130c-112">すべてのオフライン フォルダー ファイル (.ost) を含む、Microsoft Exchange ストアです。</span><span class="sxs-lookup"><span data-stu-id="2130c-112">Microsoft Exchange store, including any Offline Folder files (.ost).</span></span> 
    
-  <span data-ttu-id="2130c-113">パブリック フォルダー ストアです。</span><span class="sxs-lookup"><span data-stu-id="2130c-113">Store for public folders.</span></span> 
    
-  <span data-ttu-id="2130c-114">MSN の Microsoft Office Outlook のコネクタのストアです。</span><span class="sxs-lookup"><span data-stu-id="2130c-114">Store for Microsoft Office Outlook Connector for MSN.</span></span> 
    
 <span data-ttu-id="2130c-115">インデックスを作成するサード ・ パーティ製のストア プロバイダーは、Windows レジストリに自身を登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2130c-115">Third-party store providers that want to be indexed must register themselves in the Windows registry.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2130c-116">管理者およびユーザーは、Windows デスクトップ サーチが Outlook アイテムのインデックスを作成することを防ぐため、グループ ポリシーの設定を使用できます。</span><span class="sxs-lookup"><span data-stu-id="2130c-116">Administrators and users can use a Group Policy setting to prevent Windows Desktop Search from indexing Outlook items.</span></span> <span data-ttu-id="2130c-117">詳細については、 [Windows デスクトップ サーチの拡張](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2130c-117">For more information, see [Extending Windows Desktop Search](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx).</span></span> 
  
## <a name="registry-keys"></a><span data-ttu-id="2130c-118">レジストリ キー</span><span class="sxs-lookup"><span data-stu-id="2130c-118">Registry Keys</span></span>

<span data-ttu-id="2130c-119">コンピューターでは、Windows レジストリで次の 3 つのレジストリ キーの 1 つだけでインデックスを作成するすべてのストア プロバイダーを登録してください。</span><span class="sxs-lookup"><span data-stu-id="2130c-119">On a computer, all store providers that want to be indexed must be registered under only one of the following three registry keys in the Windows registry.</span></span> <span data-ttu-id="2130c-120">MAPI プロトコル ハンドラーは次の次の順序でこれらのキーの下にあります。</span><span class="sxs-lookup"><span data-stu-id="2130c-120">The MAPI Protocol Handler looks under each of these keys in the following order:</span></span>
  
1. <span data-ttu-id="2130c-121">[HKLM] \Software\Policies\Microsoft\Windows\Windows Search\\</span><span class="sxs-lookup"><span data-stu-id="2130c-121">[HKLM]\Software\Policies\Microsoft\Windows\Windows Search\\</span></span>
    
2. <span data-ttu-id="2130c-122">[HKLM] \Software\Microsoft\Windows\Windows Search\Preferences\\</span><span class="sxs-lookup"><span data-stu-id="2130c-122">[HKLM]\Software\Microsoft\Windows\Windows Search\Preferences\\</span></span>
    
3. <span data-ttu-id="2130c-123">[HKCU] \Software\Microsoft\Windows\Windows Search\Preferences\\</span><span class="sxs-lookup"><span data-stu-id="2130c-123">[HKCU]\Software\Microsoft\Windows\Windows Search\Preferences\\</span></span>
    
 <span data-ttu-id="2130c-124">キーの下の各値は、ストア プロバイダーがインデックスを作成することに相当します。</span><span class="sxs-lookup"><span data-stu-id="2130c-124">Each value under the key corresponds to a store provider that would be indexed.</span></span> <span data-ttu-id="2130c-125">値の名前は、グローバル一意識別子 (GUID) 0x00000001 の 16 進値には、 **DWORD**型のストア プロバイダーのです。</span><span class="sxs-lookup"><span data-stu-id="2130c-125">The name of the value is the Globally Unique Identifier (GUID) of the store provider, which is of the type **DWORD** and has the hexadecimal value 0x00000001.</span></span> 
  
## <a name="guids-for-store-providers"></a><span data-ttu-id="2130c-126">ストア プロバイダーの Guid</span><span class="sxs-lookup"><span data-stu-id="2130c-126">GUIDs for Store Providers</span></span>

<span data-ttu-id="2130c-127">**[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** の MAPI プロパティは、MAPI ストアの GUID を指定します。</span><span class="sxs-lookup"><span data-stu-id="2130c-127">The MAPI property **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** specifies the GUID of a MAPI store.</span></span> <span data-ttu-id="2130c-128">Outlook のインデックスが次の表に記載されているストア プロバイダーの Guid です。</span><span class="sxs-lookup"><span data-stu-id="2130c-128">The GUIDs for the store providers that Outlook indexes are described in the following table.</span></span> 
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="2130c-129">**ストア プロバイダーの種類**</span><span class="sxs-lookup"><span data-stu-id="2130c-129">**Type of Store Provider**</span></span> <br/> |<span data-ttu-id="2130c-130">**GUID**</span><span class="sxs-lookup"><span data-stu-id="2130c-130">**GUID**</span></span> <br/> |<span data-ttu-id="2130c-131">**メモ**</span><span class="sxs-lookup"><span data-stu-id="2130c-131">**Notes**</span></span> <br/> |
|<span data-ttu-id="2130c-132">個人用フォルダー ファイル (。PST)</span><span class="sxs-lookup"><span data-stu-id="2130c-132">Personal Folders files (.PST)</span></span>  <br/> |<span data-ttu-id="2130c-133">{4154494E-BFF9-01B8-00AA-0037D96E0000}</span><span class="sxs-lookup"><span data-stu-id="2130c-133">{4154494E-BFF9-01B8-00AA-0037D96E0000}</span></span>  <br/> |<span data-ttu-id="2130c-134">GUID が**MSPST_UID_PROVIDER**として、パブリック ヘッダー ファイル mspst.h に記載されています。</span><span class="sxs-lookup"><span data-stu-id="2130c-134">GUID is documented in the public header file mspst.h as **MSPST_UID_PROVIDER**</span></span> <br/> |
|<span data-ttu-id="2130c-135">Exchange</span><span class="sxs-lookup"><span data-stu-id="2130c-135">Exchange</span></span>  <br/> |<span data-ttu-id="2130c-136">{C0A19454-7F29-1B10-A587-08002B2A2517}</span><span class="sxs-lookup"><span data-stu-id="2130c-136">{C0A19454-7F29-1B10-A587-08002B2A2517}</span></span>  <br/> |<span data-ttu-id="2130c-137">GUID が**pbExchangeProviderPrimaryUserGuid**として、パブリック ヘッダー ファイル edkmdb.h に記載されています。</span><span class="sxs-lookup"><span data-stu-id="2130c-137">GUID is documented in the public header file edkmdb.h as **pbExchangeProviderPrimaryUserGuid**</span></span> <br/> |
|<span data-ttu-id="2130c-138">パブリック フォルダー</span><span class="sxs-lookup"><span data-stu-id="2130c-138">Public folders</span></span>  <br/> |<span data-ttu-id="2130c-139">{70fab278-f7af-cd11-9bc8-00aa002fc45a}</span><span class="sxs-lookup"><span data-stu-id="2130c-139">{70fab278-f7af-cd11-9bc8-00aa002fc45a}</span></span>  <br/> |<span data-ttu-id="2130c-140">GUID が**pbExchangeProviderPublicGuid**として、パブリック ヘッダー ファイル edkmdb.h に記載されています。</span><span class="sxs-lookup"><span data-stu-id="2130c-140">GUID is documented in the public header file edkmdb.h as **pbExchangeProviderPublicGuid**</span></span> <br/> |
|<span data-ttu-id="2130c-141">の</span><span class="sxs-lookup"><span data-stu-id="2130c-141">Outlook Connector for MSN</span></span>  <br/> |<span data-ttu-id="2130c-142">{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}</span><span class="sxs-lookup"><span data-stu-id="2130c-142">{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}</span></span>  <br/> |<span data-ttu-id="2130c-143">なし</span><span class="sxs-lookup"><span data-stu-id="2130c-143">None</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2130c-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="2130c-144">See also</span></span>



[<span data-ttu-id="2130c-145">ストア API について</span><span class="sxs-lookup"><span data-stu-id="2130c-145">About the Store API</span></span>](about-the-store-api.md)

