---
title: ユーザー設定のフォーム定義を保存し、メッセージを削除します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6a270f0c-104a-84a1-9adf-aea166f89071
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: 9581656c40af39338f8919903f6d0de29c20a061
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800254"
---
# <a name="remove-custom-form-definition-saved-with-a-message"></a><span data-ttu-id="aad11-103">ユーザー設定のフォーム定義を保存し、メッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="aad11-103">Remove custom form definition saved with a message</span></span>
  
<span data-ttu-id="aad11-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aad11-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aad11-105">このトピックでは、フォーム定義を含まない通常のメッセージにユーザー設定のフォーム定義に保存されているメッセージに変換する C++ のコード例を示します。</span><span class="sxs-lookup"><span data-stu-id="aad11-105">This topic shows a code sample in C++ that converts a message that has been saved with a custom form definition to a regular message without the form definition.</span></span>
  
<span data-ttu-id="aad11-106">Microsoft Outlook 2010 または Microsoft Outlook 2013 では、フォーム ライブラリに発行すること、または、メッセージに対応するフォーム定義を保存してユーザー設定フォームのページを含むフォームを共有できます。</span><span class="sxs-lookup"><span data-stu-id="aad11-106">In Microsoft Outlook 2010 or Microsoft Outlook 2013, you can share forms containing custom form pages by either publishing them to a forms library or saving the corresponding form definition with a message.</span></span> <span data-ttu-id="aad11-107">メッセージと共に保存されるカスタム フォームが一般的と呼ばれる「one-off フォーム、」1 回限りのインスタンスとその特定のメッセージを表示するだけのフォームを共有するため。</span><span class="sxs-lookup"><span data-stu-id="aad11-107">A custom form saved with a message is commonly referred as a "one-off form", since the form is shared only for viewing that specific message as a one-off instance.</span></span> <span data-ttu-id="aad11-108">通常これを行うフォームをフォーム ライブラリに発行されませんが、受信者がアイテムを開くときにユーザー設定フォームを使用するとします。</span><span class="sxs-lookup"><span data-stu-id="aad11-108">You typically do this when the form is not published in a forms library but you want the recipient to use the custom form when opening the item.</span></span> <span data-ttu-id="aad11-109">フォームは、フォームの [**プロパティ**] ページで [**アイテムのフォーム レイアウトも送信**] チェック ボックスを選択して one-off フォーム デザイナーで指定できます。</span><span class="sxs-lookup"><span data-stu-id="aad11-109">You can specify a form is a one-off in the Forms Designer, by selecting the **Send form definition with item** check box on the **Properties** page of the form.</span></span> 
  
<span data-ttu-id="aad11-110">フォーム ページを含むフォームをカスタマイズするには、Visual Basic Scripting Edition (VBScript) 内のコードとします。</span><span class="sxs-lookup"><span data-stu-id="aad11-110">Forms containing form pages can be customized with code in Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="aad11-111">フォーム定義が保存されているメッセージは、一般的にサイズが大きくします。</span><span class="sxs-lookup"><span data-stu-id="aad11-111">Messages that are saved with form definitions are generally bigger in size.</span></span> <span data-ttu-id="aad11-112">セキュリティおよびストレージ上の理由から、Outlook 2010、Outlook 2013 は、フォーム定義がアイテムと共に保存を無視します。</span><span class="sxs-lookup"><span data-stu-id="aad11-112">For security and storage reasons, Outlook 2010 and Outlook 2013 ignore form definitions saved with any item.</span></span>
  
<span data-ttu-id="aad11-113">ないユーザー設定のフォーム定義に保存されているメッセージを変換するには、4 つの名前付きプロパティを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aad11-113">To convert a message that is saved with a custom form definition to one without, you must remove four named properties:</span></span>
  
- [<span data-ttu-id="aad11-114">PidLidFormStorage ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="aad11-114">PidLidFormStorage Canonical Property</span></span>](pidlidformstorage-canonical-property.md)
    
- [<span data-ttu-id="aad11-115">PidLidPageDirStream ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="aad11-115">PidLidPageDirStream Canonical Property</span></span>](pidlidpagedirstream-canonical-property.md)
    
- [<span data-ttu-id="aad11-116">PidLidFormPropStream ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="aad11-116">PidLidFormPropStream Canonical Property</span></span>](pidlidformpropstream-canonical-property.md)
    
- [<span data-ttu-id="aad11-117">PidLidScriptStream ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="aad11-117">PidLidScriptStream Canonical Property</span></span>](pidlidscriptstream-canonical-property.md)
    
<span data-ttu-id="aad11-118">さらに、そのメッセージを保存するカスタム プロパティの定義が含まれています[PidLidPropertyDefinitionStream の標準的なプロパティ](pidlidpropertydefinitionstream-canonical-property.md)を削除することもする必要があります。</span><span class="sxs-lookup"><span data-stu-id="aad11-118">In addition, you should also remove the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md) that contains the definitions of custom properties saved with that message.</span></span> <span data-ttu-id="aad11-119">このプロパティを削除することの副次的な影響を Outlook 2010 または Outlook 2013 オブジェクト モデルは、Outlook 2010 または Outlook 2013 のユーザー インターフェイスは、メッセージに設定されているユーザー プロパティにアクセスすることができなきます。</span><span class="sxs-lookup"><span data-stu-id="aad11-119">A side effect of removing this property is that the Outlook 2010 or Outlook 2013 object models and the Outlook 2010 or Outlook 2013 user interface will no longer be able to access user properties that have been set on the message.</span></span> <span data-ttu-id="aad11-120">まだ MAPI を介してこれらのプロパティとその値にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="aad11-120">You are still able to access these properties and their values through MAPI.</span></span> <span data-ttu-id="aad11-121">このプロパティを削除しないし、別のフォーム定義を使用してメッセージを保存、 [PidLidPropertyDefinitionStream の標準的なプロパティ](pidlidpropertydefinitionstream-canonical-property.md)は、部分的に新しいデータで上書きに注意してくださいし、データの整合性は保証されません。</span><span class="sxs-lookup"><span data-stu-id="aad11-121">Note that if you do not remove this property and the message is saved with another form definition, the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md) is partially overwritten with new data and data integrity is not guaranteed.</span></span> 
  
<span data-ttu-id="aad11-122">[PidLidPropertyDefinitionStream の標準的なプロパティ](pidlidpropertydefinitionstream-canonical-property.md)を削除する場合、 [PidLidCustomFlag の標準的なプロパティ](pidlidcustomflag-canonical-property.md)から**INSP_PROPDEFINITION**フラグも削除必要があります。</span><span class="sxs-lookup"><span data-stu-id="aad11-122">If you remove the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md), then you should also remove the **INSP_PROPDEFINITION** flag from the [PidLidCustomFlag Canonical Property](pidlidcustomflag-canonical-property.md).</span></span>
  
<span data-ttu-id="aad11-123">次の関数では、 `RemoveOneOff`、受け入れる入力パラメーターとしてメッセージとインジケーターへのポインター、 [PidLidPropertyDefinitionStream の標準的なプロパティ](pidlidpropertydefinitionstream-canonical-property.md)を削除するかどうか。</span><span class="sxs-lookup"><span data-stu-id="aad11-123">The following function,  `RemoveOneOff`, accepts as input parameters a pointer to a message and an indicator whether to remove the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md).</span></span> <span data-ttu-id="aad11-124">メッセージ ポインターを使用して、適切なプロパティの識別子を取得する[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を呼び出す、名前付きプロパティを削除するのには[IMAPIProp::DeleteProps](imapiprop-deleteprops.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="aad11-124">Using the message pointer, it calls [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the appropriate property identifiers, and then calls [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) to remove the named properties.</span></span> <span data-ttu-id="aad11-125">また[PidLidCustomFlag の標準的なプロパティ](pidlidcustomflag-canonical-property.md)を取得する[IMAPIProp::GetProps](imapiprop-getprops.md)を呼び出すし、クリア、 **INSP\_ONEOFFFLAGS**フラグは、 **INSP_PROPDEFINITION**としてフラグを設定、そのプロパティの適切なので、Outlook 2010 と削除されたこれらの名前付きプロパティの outlook 2013 を検索しません。</span><span class="sxs-lookup"><span data-stu-id="aad11-125">It also calls [IMAPIProp::GetProps](imapiprop-getprops.md) to get the [PidLidCustomFlag Canonical Property](pidlidcustomflag-canonical-property.md) and clears the **INSP\_ONEOFFFLAGS** flag and **INSP_PROPDEFINITION** flag as appropriate from that property, so that Outlook 2010 and Outlook 2013 will not look for those named properties that have been removed.</span></span> 
  
```cpp
ULONG aulOneOffIDs[] = {dispidFormStorage,  
    dispidPageDirStream, 
    dispidFormPropStream, 
    dispidScriptStream, 
    dispidPropDefStream, // dispidPropDefStream must remain next to last in list 
    dispidCustomFlag};   // dispidCustomFlag must remain last in list 
 
#define ulNumOneOffIDs (sizeof(aulOneOffIDs)/sizeof(aulOneOffIDs[0])) 
 
HRESULT RemoveOneOff(LPMESSAGE lpMessage, BOOL bRemovePropDef) 
{ 
    if (!lpMessage) return MAPI_E_INVALID_PARAMETER; 
     
    HRESULT hRes = S_OK; 
    MAPINAMEID  rgnmid[ulNumOneOffIDs]; 
    LPMAPINAMEID rgpnmid[ulNumOneOffIDs]; 
    LPSPropTagArray lpTags = NULL; 
 
    ULONG i = 0; 
    for (i = 0 ; i < ulNumOneOffIDs ; i++) 
    { 
        rgnmid[i].lpguid = (LPGUID)&PSETID_Common; 
        rgnmid[i].ulKind = MNID_ID; 
        rgnmid[i].Kind.lID = aulOneOffIDs[i]; 
        rgpnmid[i] = &rgnmid[i]; 
    } 
   
    hRes = lpMessage->GetIDsFromNames( 
        ulNumOneOffIDs, 
        rgpnmid, 
        0, 
        &lpTags); 
    if (lpTags) 
    { 
        // The last prop is the flag value  
        // to be updated, don't count it 
        lpTags->cValues = ulNumOneOffIDs-1; 
 
        // If the prop def stream is not to be removed, don't count it 
        if (!bRemovePropDef) 
        { 
          lpTags->cValues = lpTags->cValues-1; 
        } 
 
        hRes = lpMessage->DeleteProps( 
            lpTags, 
            0); 
        if (SUCCEEDED(hRes)) 
        { 
            SPropTagArray pTag = {0}; 
            ULONG cProp = 0; 
            LPSPropValue lpCustomFlag = NULL; 
 
            // Grab dispidCustomFlag, the last tag in the array 
            pTag.cValues = 1; 
            pTag.aulPropTag[0] = CHANGE_PROP_TYPE( 
                lpTags->aulPropTag[ulNumOneOffIDs-1], 
                PT_LONG); 
 
            hRes = lpMessage->GetProps( 
                &pTag, 
                fMapiUnicode, 
                &cProp, 
                &lpCustomFlag); 
            if (SUCCEEDED(hRes) &&  
                1 == cProp && lpCustomFlag &&  
                PT_LONG == PROP_TYPE(lpCustomFlag->ulPropTag)) 
            { 
                // Clear the INSP_ONEOFFFLAGS bits so Outlook  
                // doesn't look for the props that have been deleted 
                lpCustomFlag->Value.l =  
                    lpCustomFlag->Value.l & ~(INSP_ONEOFFFLAGS); 
                if (bRemovePropDef) 
                { 
                    lpCustomFlag->Value.l =  
                        lpCustomFlag->Value.l & ~(INSP_PROPDEFINITION); 
                } 
                hRes = lpMessage->SetProps( 
                    1, 
                    lpCustomFlag, 
                    NULL); 
             } 
 
             hRes = lpMessage->SaveChanges(KEEP_OPEN_READWRITE); 
         } 
    } 
    MAPIFreeBuffer(lpTags); 
 
    return hRes; 
}
```

## <a name="see-also"></a><span data-ttu-id="aad11-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="aad11-126">See also</span></span>

- [<span data-ttu-id="aad11-127">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="aad11-127">MAPI Constants</span></span>](mapi-constants.md)

