---
title: 制限のサンプル コード
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9b82097c-dbd6-4ba0-a6cb-292301f9402b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 4f41abe2ee41946f68e1d79c75b36791364ea970
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803786"
---
# <a name="sample-restriction-code"></a><span data-ttu-id="d1cda-103">制限のサンプル コード</span><span class="sxs-lookup"><span data-stu-id="d1cda-103">Sample restriction code</span></span>

<span data-ttu-id="d1cda-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d1cda-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d1cda-105">次のサンプル コードは、件名に「バレーボール」という単語が含まれていないすべてのメッセージをフィルターする制約を作成する方法を示していますし、、Sam から政美に送信されなかった。</span><span class="sxs-lookup"><span data-stu-id="d1cda-105">The following sample code shows how to create a restriction that filters out all messages that do not contain the word "volleyball" in the subject line and were not sent to Sue from Sam.</span></span> <span data-ttu-id="d1cda-106">[SRestriction](srestriction.md)構造のツリーは、 [SAndRestriction](sandrestriction.md)構造体を使用して実装、**および**制限をされている最上位のノードを持つ必要は。</span><span class="sxs-lookup"><span data-stu-id="d1cda-106">A tree of [SRestriction](srestriction.md) structures is required, with the top node being an **AND** restriction implemented with an [SAndRestriction](sandrestriction.md) structure.</span></span> <span data-ttu-id="d1cda-107">政美に送信されたメッセージを検索するサブオブジェクトの制限、Sam からのメッセージを検索するコンテンツの制限とメッセージを検索するもう 1 つ**と**制限は、 **AND**演算で結ばれている 3 つの制限「バレーボール」を含む件名が指定されています。</span><span class="sxs-lookup"><span data-stu-id="d1cda-107">The three restrictions that are joined by the **AND** operation are a subobject restriction that searches for messages sent to Sue, a content restriction that searches for messages from Sam, and another **AND** restriction that searches for messages that have a subject containing "volleyball."</span></span> <span data-ttu-id="d1cda-108">**あるの PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) は、必要なプロパティではないため、**既存**の制限に含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1cda-108">Because **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) is not a required property, an **Exist** restriction must be included.</span></span> 
  
<span data-ttu-id="d1cda-109">このコードを使用して、動的な割り当てと初期化します。割り当ておよび同様に静的に初期化することはできます。</span><span class="sxs-lookup"><span data-stu-id="d1cda-109">This code uses dynamic allocation and initialization; it is possible to allocate and initialize statically as well.</span></span> <span data-ttu-id="d1cda-110">簡潔に、次に発生する必要がありますエラーのチェック割り当て呼び出しに含まれていないサンプルです。</span><span class="sxs-lookup"><span data-stu-id="d1cda-110">In the interest of brevity, the error checking that must occur following the allocation calls is not included in the sample.</span></span> 
  
```cpp
HRESULT BuildRestriction (LPSTR pszSent, LPSTR pszFrom,
                                LPSTR pszSubjectText);
{
    LPSRestriction pRest, pAndRes, pObjRes, pSubjAndRes;
    LPSPropValue pRecip, pSender, pSubject;
    HRESULT hResult;
    ULONG ulResCount = 3, ulSubjCount = 2
    // Allocate and build  restriction to join criteria
    hResult = MAPIAllocateMore (sizeof(SRestriction)*ulResCount, pRest,
            (LPVOID *)&pAndRes);
    pRest->rt = RES_AND;
    pRest->res.resAnd.cRes = ulResCount;
    pRest->res.resAnd.lpRes = pAndRes;
    // Allocate and build subobject restriction to search recipient list
    hResult = MAPIAllocateMore (sizeof(SRestriction), pRest,
            (LPVOID *)&pObjRes);
    pAndRes[0].rt = RES_SUBRESTRICTION;
    pAndRes[0].res.resSub.ulSubObject = PR_MESSAGE_RECIPIENTS;
    pAndRes[0].res.resSub.lpRes = pObjRes;
    // Allocate and build content restriction to look for recipient
    hResult = MAPIAllocateMore (sizeof(SPropValue), pRest,
            (LPVOID *)&pRecip);
    pObjRes->rt = RES_CONTENT;
    pObjRes->res.resContent.ulFuzzyLevel =
            FL_FULLSTRING | FL_IGNORECASE;
    pObjRes->res.resContent.ulPropTag = pRecip->ulPropTag =
            PR_DISPLAY_NAME;
    pObjRes->res.resContent.lpProp = pRecip;
    pRecip->Value.LPSZ = pszSent;              // pszSent set to Sue
    // Allocate and build content restriction to look for sender
    hResult = MAPIAllocateMore (sizeof(SPropValue), pRest,
            (LPVOID *)&pSend);
    pAndRes[1].rt = RES_CONTENT;
    pAndRes[1].res.resContent.ulFuzzyLevel =
            FL_FULLSTRING | FL_IGNORECASE;
    pAndRes[1].res.resContent.ulPropTag = pSend->ulPropTag =
            PR_SENDER_NAME;
    pAndRes[1].res.resContent.lpProp = pSend;
    pSend->Value.LPSZ = pszName;                    // pszName set to Sam
    // Allocate and build  restriction to look for subject
    hResult = MAPIAllocateMore (sizeof(SRestriction)*ulSubjCount, pRest,
            (LPVOID *)&pSubjAndRes);
    pRest->rt = RES_AND;
    pRest->res.resAnd.cRes = ulResCount;
    pRest->res.resAnd.lpRes = pAndRes;
    // Create an  restriction to search for subject
    hResult = MAPIAllocateMore (sizeof(SPropValue), pRest,
            (LPVOID *)&pSubjAndRes);
    pAndRes[2].rt = RES_AND;
    pAndRes[2].res.resAnd.cRes = ulSubjCount;
    pAndRes[2].res.resAnd.lpRes = pSubjAndRes;
    // Exist restriction to check that PR_SUBJECT exists
    hResult = MAPIAllocateMore (sizeof(SPropValue), pRest,
            (LPVOID *)&pSubj);
    pSubjAndRes[0].rt = RES_EXIST;
    pSubjAndRes[0].res.resExist.ulReserved1 = 0;
    pSubjAndRes[0].res.resExist.ulReserved2 = 0;
    pSubjAndRes[0].res.resExist.ulPropTag = PR_SUBJECT;
    // Content restriction to check for "volleyball" in subject
    hResult = MAPIAllocateMore (sizeof(SPropValue), pRest,
            (LPVOID *)&pSubj);
    pSubjAndRes[1].res.resContent.ulFuzzyLevel =
            FL_SUBSTRING | FL_IGNORECASE;
    pSubjAndRes[1].res.resContent.ulPropTag = pSubj->ulPropTag =
            PR_SUBJECT;
    pSubjAndRes[1].res.resContent.lpProp = pSubj;
    pSubj->Value.LPSZ = pszSubjectText;
    return hResult;
}
 
```

## <a name="see-also"></a><span data-ttu-id="d1cda-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="d1cda-111">See also</span></span>

- [<span data-ttu-id="d1cda-112">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="d1cda-112">MAPI Tables</span></span>](mapi-tables.md)

