---
title: MAPI プロパティの保存
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ed0c14f9-3dcf-49ad-928e-ba872d4d6b5a
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 6135dfae915a1e70743f9224352390c4b56ea02e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803795"
---
# <a name="saving-mapi-properties"></a><span data-ttu-id="dcc98-103">MAPI プロパティの保存</span><span class="sxs-lookup"><span data-stu-id="dcc98-103">Saving MAPI Properties</span></span>

  
  
<span data-ttu-id="dcc98-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dcc98-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dcc98-105">多くのオブジェクトは、トランザクション モデルのため、プロパティを変更できない永続的なものは後でコミットされるまでの処理をサポートします。</span><span class="sxs-lookup"><span data-stu-id="dcc98-105">Many objects support a transaction model of processing whereby changes to properties are not made permanent until they are committed at a later time.</span></span> <span data-ttu-id="dcc98-106">プロパティへの変更は、 [IMAPIProp::SetProps](imapiprop-setprops.md)および[IMAPIProp::DeleteProps](imapiprop-deleteprops.md)メソッドは、一方、commit の手順は、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)によって処理されます。</span><span class="sxs-lookup"><span data-stu-id="dcc98-106">Whereas changes to properties are handled by the [IMAPIProp::SetProps](imapiprop-setprops.md) and [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) methods, the commit step is handled by [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="dcc98-107">**失敗 savechanges メソッド**の呼び出し、最新のオブジェクトのプロパティにアクセスできることが終了するまでではありません。</span><span class="sxs-lookup"><span data-stu-id="dcc98-107">It isn't until after a successful call to **SaveChanges** that the most recent version of an object's properties can be accessed.</span></span> 
  
<span data-ttu-id="dcc98-108">**SaveChanges**には、エラー値 MAPI_E_OBJECT_CHANGED が返された、これは、する別のクライアントが同時に変更をコミットするオブジェクトに警告します。</span><span class="sxs-lookup"><span data-stu-id="dcc98-108">When **SaveChanges** returns the error value MAPI_E_OBJECT_CHANGED, this is a warning that another client is simultaneously committing changes to the object.</span></span> <span data-ttu-id="dcc98-109">可能性が、複数のクライアントに対して、オブジェクトを実装すると、正常にプロバイダーによってオブジェクトを開くメソッドを呼び出して、 **OpenEntry** 、MAPI_MODIFY フラグを設定して読み取り/書き込みアクセス許可を付与します。</span><span class="sxs-lookup"><span data-stu-id="dcc98-109">It is possible, depending on the provider implementing the object, for multiple clients to successfully open an object by calling its **OpenEntry** method with the MAPI_MODIFY flag set, giving them read/write access.</span></span> <span data-ttu-id="dcc98-110">**OpenEntry**呼び出しは、ストレージ ・ データのスナップショットではこのような返されるオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="dcc98-110">The object that is returned from such an **OpenEntry** call is a snapshot of the storage data.</span></span> <span data-ttu-id="dcc98-111">各とするとこのデータを変更するには、以前の試みを上書きできます。</span><span class="sxs-lookup"><span data-stu-id="dcc98-111">Each subsequent attempt to change this data can overwrite the previous attempt.</span></span> 
  
<span data-ttu-id="dcc98-112">クライアントでは、 **SaveChanges**から MAPI_E_OBJECT_CHANGED を受信時にするオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="dcc98-112">Upon receiving MAPI_E_OBJECT_CHANGED from **SaveChanges**, a client has the option to:</span></span> 
  
- <span data-ttu-id="dcc98-113">変更を保持するオブジェクトのコピーを作成します。</span><span class="sxs-lookup"><span data-stu-id="dcc98-113">Make a copy of the object to hold the changes.</span></span>
    
- <span data-ttu-id="dcc98-114">**SaveChanges**FORCE_SAVE を指定する別の呼び出しを確認します。</span><span class="sxs-lookup"><span data-stu-id="dcc98-114">Make another call to **SaveChanges**, specifying FORCE_SAVE.</span></span> 
    
<span data-ttu-id="dcc98-115">FORCE_SAVE フラグを使用して**SaveChanges**を呼び出すことでは、前回の保存が上書きされ、クライアントの変更を永続的になります。</span><span class="sxs-lookup"><span data-stu-id="dcc98-115">Calling **SaveChanges** with the FORCE_SAVE flag overwrites the previous save and makes a client's changes permanent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dcc98-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="dcc98-116">See also</span></span>



[<span data-ttu-id="dcc98-117">MAPI のプロパティの概要</span><span class="sxs-lookup"><span data-stu-id="dcc98-117">MAPI Property Overview</span></span>](mapi-property-overview.md)

