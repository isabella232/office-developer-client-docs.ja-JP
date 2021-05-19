---
title: MAPI プロパティの保存
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ed0c14f9-3dcf-49ad-928e-ba872d4d6b5a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5d4653492028151d7e19a5d5490c8c8949002a4f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425891"
---
# <a name="saving-mapi-properties"></a><span data-ttu-id="82235-103">MAPI プロパティの保存</span><span class="sxs-lookup"><span data-stu-id="82235-103">Saving MAPI Properties</span></span>

  
  
<span data-ttu-id="82235-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82235-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82235-105">多くのオブジェクトは処理のトランザクション モデルをサポートしています。その結果、プロパティに対する変更は、後でコミットされるまで永続化されません。</span><span class="sxs-lookup"><span data-stu-id="82235-105">Many objects support a transaction model of processing whereby changes to properties are not made permanent until they are committed at a later time.</span></span> <span data-ttu-id="82235-106">プロパティへの変更は [IMAPIProp::SetProps](imapiprop-setprops.md) メソッドと [IMAPIProp::D eleteProps](imapiprop-deleteprops.md) メソッドによって処理されるのに対し、コミット ステップは [IMAPIProp::SaveChanges](imapiprop-savechanges.md)によって処理されます。</span><span class="sxs-lookup"><span data-stu-id="82235-106">Whereas changes to properties are handled by the [IMAPIProp::SetProps](imapiprop-setprops.md) and [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) methods, the commit step is handled by [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="82235-107">**SaveChanges** の呼び出しが成功するまで、オブジェクトのプロパティの最新バージョンにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="82235-107">It isn't until after a successful call to **SaveChanges** that the most recent version of an object's properties can be accessed.</span></span> 
  
<span data-ttu-id="82235-108">**SaveChanges が** エラー値を返MAPI_E_OBJECT_CHANGED、これは、別のクライアントがオブジェクトに対する変更を同時にコミットしているという警告です。</span><span class="sxs-lookup"><span data-stu-id="82235-108">When **SaveChanges** returns the error value MAPI_E_OBJECT_CHANGED, this is a warning that another client is simultaneously committing changes to the object.</span></span> <span data-ttu-id="82235-109">オブジェクトを実装するプロバイダーによっては、複数のクライアントが MAPI_MODIFY フラグ セットを使用して **OpenEntry** メソッドを呼び出してオブジェクトを正常に開き、読み取り/書き込みアクセス権を与えることも可能です。</span><span class="sxs-lookup"><span data-stu-id="82235-109">It is possible, depending on the provider implementing the object, for multiple clients to successfully open an object by calling its **OpenEntry** method with the MAPI_MODIFY flag set, giving them read/write access.</span></span> <span data-ttu-id="82235-110">このような **OpenEntry** 呼び出しから返されるオブジェクトは、ストレージ データのスナップショットです。</span><span class="sxs-lookup"><span data-stu-id="82235-110">The object that is returned from such an **OpenEntry** call is a snapshot of the storage data.</span></span> <span data-ttu-id="82235-111">以降、このデータを変更しようとすると、以前の試行が上書きされる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="82235-111">Each subsequent attempt to change this data can overwrite the previous attempt.</span></span> 
  
<span data-ttu-id="82235-112">**SaveChanges** MAPI_E_OBJECT_CHANGED受信すると、クライアントは次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="82235-112">Upon receiving MAPI_E_OBJECT_CHANGED from **SaveChanges**, a client has the option to:</span></span> 
  
- <span data-ttu-id="82235-113">変更を保持するオブジェクトのコピーを作成します。</span><span class="sxs-lookup"><span data-stu-id="82235-113">Make a copy of the object to hold the changes.</span></span>
    
- <span data-ttu-id="82235-114">SaveChanges に別の **呼び出しを行** い、名前をFORCE_SAVE。</span><span class="sxs-lookup"><span data-stu-id="82235-114">Make another call to **SaveChanges**, specifying FORCE_SAVE.</span></span> 
    
<span data-ttu-id="82235-115">**SaveChanges を呼** び出して FORCE_SAVEフラグを指定すると、以前の保存が上書きされ、クライアントの変更が永続的になります。</span><span class="sxs-lookup"><span data-stu-id="82235-115">Calling **SaveChanges** with the FORCE_SAVE flag overwrites the previous save and makes a client's changes permanent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="82235-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="82235-116">See also</span></span>



[<span data-ttu-id="82235-117">MAPI のプロパティの概要</span><span class="sxs-lookup"><span data-stu-id="82235-117">MAPI Property Overview</span></span>](mapi-property-overview.md)

