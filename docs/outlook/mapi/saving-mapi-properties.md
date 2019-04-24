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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283087"
---
# <a name="saving-mapi-properties"></a><span data-ttu-id="60c31-103">MAPI プロパティの保存</span><span class="sxs-lookup"><span data-stu-id="60c31-103">Saving MAPI Properties</span></span>

  
  
<span data-ttu-id="60c31-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="60c31-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="60c31-105">多くのオブジェクトは処理のトランザクションモデルをサポートしているため、プロパティへの変更は後でコミットされるまで永続的に行われません。</span><span class="sxs-lookup"><span data-stu-id="60c31-105">Many objects support a transaction model of processing whereby changes to properties are not made permanent until they are committed at a later time.</span></span> <span data-ttu-id="60c31-106">プロパティへの変更は[imapiprop:: setprops](imapiprop-setprops.md)メソッドと[imapiprop::D eleteprops](imapiprop-deleteprops.md)メソッドによって処理されますが、コミット手順は[imapiprop:: SaveChanges](imapiprop-savechanges.md)によって処理されます。</span><span class="sxs-lookup"><span data-stu-id="60c31-106">Whereas changes to properties are handled by the [IMAPIProp::SetProps](imapiprop-setprops.md) and [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) methods, the commit step is handled by [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="60c31-107">これは、オブジェクトのプロパティの最新バージョンにアクセスできるように**SaveChanges**を正常に呼び出した後には行われません。</span><span class="sxs-lookup"><span data-stu-id="60c31-107">It isn't until after a successful call to **SaveChanges** that the most recent version of an object's properties can be accessed.</span></span> 
  
<span data-ttu-id="60c31-108">**SaveChanges**がエラー値 MAPI_E_OBJECT_CHANGED を返す場合、これは、別のクライアントがオブジェクトへの変更を同時にコミットしていることを示す警告です。</span><span class="sxs-lookup"><span data-stu-id="60c31-108">When **SaveChanges** returns the error value MAPI_E_OBJECT_CHANGED, this is a warning that another client is simultaneously committing changes to the object.</span></span> <span data-ttu-id="60c31-109">オブジェクトを実装するプロバイダーによっては、MAPI_MODIFY フラグが設定された**openentry**メソッドを呼び出して読み取り/書き込みアクセス権を付与することによって、複数のクライアントがオブジェクトを正常に開くことができます。</span><span class="sxs-lookup"><span data-stu-id="60c31-109">It is possible, depending on the provider implementing the object, for multiple clients to successfully open an object by calling its **OpenEntry** method with the MAPI_MODIFY flag set, giving them read/write access.</span></span> <span data-ttu-id="60c31-110">このような**openentry**呼び出しから返されるオブジェクトは、ストレージデータのスナップショットです。</span><span class="sxs-lookup"><span data-stu-id="60c31-110">The object that is returned from such an **OpenEntry** call is a snapshot of the storage data.</span></span> <span data-ttu-id="60c31-111">このデータを以降に変更しようとするたびに、以前の試行を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="60c31-111">Each subsequent attempt to change this data can overwrite the previous attempt.</span></span> 
  
<span data-ttu-id="60c31-112">MAPI_E_OBJECT_CHANGED を**SaveChanges**から受け取る際に、クライアントには次のオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="60c31-112">Upon receiving MAPI_E_OBJECT_CHANGED from **SaveChanges**, a client has the option to:</span></span> 
  
- <span data-ttu-id="60c31-113">変更を保持するオブジェクトのコピーを作成します。</span><span class="sxs-lookup"><span data-stu-id="60c31-113">Make a copy of the object to hold the changes.</span></span>
    
- <span data-ttu-id="60c31-114">FORCE_SAVE を指定して、再度、 **SaveChanges**を呼び出してください。</span><span class="sxs-lookup"><span data-stu-id="60c31-114">Make another call to **SaveChanges**, specifying FORCE_SAVE.</span></span> 
    
<span data-ttu-id="60c31-115">FORCE_SAVE フラグを使用して**SaveChanges**を呼び出すと、以前の保存が上書きされ、クライアントの変更が永続的に行われます。</span><span class="sxs-lookup"><span data-stu-id="60c31-115">Calling **SaveChanges** with the FORCE_SAVE flag overwrites the previous save and makes a client's changes permanent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="60c31-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="60c31-116">See also</span></span>



[<span data-ttu-id="60c31-117">MAPI のプロパティの概要</span><span class="sxs-lookup"><span data-stu-id="60c31-117">MAPI Property Overview</span></span>](mapi-property-overview.md)

