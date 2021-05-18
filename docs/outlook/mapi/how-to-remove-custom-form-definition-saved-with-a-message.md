---
title: メッセージと共に保存されているユーザー設定フォーム定義を削除する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6a270f0c-104a-84a1-9adf-aea166f89071
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: ac162cb73cfdee83bf034de32064c5ed9df3bc02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408468"
---
# <a name="remove-custom-form-definition-saved-with-a-message"></a><span data-ttu-id="78783-103">メッセージと共に保存されているユーザー設定フォーム定義を削除する</span><span class="sxs-lookup"><span data-stu-id="78783-103">Remove custom form definition saved with a message</span></span>
  
<span data-ttu-id="78783-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78783-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78783-105">このトピックでは、カスタム フォーム定義で保存されたメッセージを、フォーム定義なしで通常のメッセージに変換する C++ のコード サンプルを示します。</span><span class="sxs-lookup"><span data-stu-id="78783-105">This topic shows a code sample in C++ that converts a message that has been saved with a custom form definition to a regular message without the form definition.</span></span>
  
<span data-ttu-id="78783-106">ユーザー Microsoft Outlook 2010またはMicrosoft Outlook 2013、カスタム フォーム ページを含むフォームを共有するには、カスタム フォーム ページをフォーム ライブラリに発行するか、対応するフォーム定義をメッセージで保存します。</span><span class="sxs-lookup"><span data-stu-id="78783-106">In Microsoft Outlook 2010 or Microsoft Outlook 2013, you can share forms containing custom form pages by either publishing them to a forms library or saving the corresponding form definition with a message.</span></span> <span data-ttu-id="78783-107">メッセージと一緒に保存されたカスタム フォームは、その特定のメッセージを 1 回限りインスタンスとして表示するためにのみ共有されるので、一般に"1 回限りフォーム" と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="78783-107">A custom form saved with a message is commonly referred as a "one-off form", since the form is shared only for viewing that specific message as a one-off instance.</span></span> <span data-ttu-id="78783-108">通常、フォームがフォーム ライブラリで発行されていないが、アイテムを開く際に受信者がカスタム フォームを使用する場合にこれを行います。</span><span class="sxs-lookup"><span data-stu-id="78783-108">You typically do this when the form is not published in a forms library but you want the recipient to use the custom form when opening the item.</span></span> <span data-ttu-id="78783-109">フォームの [プロパティ] ページの [アイテムを使用してフォーム定義を送信する] チェック ボックスをオンにすると、フォームがフォーム デザイナーで 1 回切り替えで指定できます。</span><span class="sxs-lookup"><span data-stu-id="78783-109">You can specify a form is a one-off in the Forms Designer, by selecting the **Send form definition with item** check box on the **Properties** page of the form.</span></span> 
  
<span data-ttu-id="78783-110">フォーム ページを含むフォームは、スクリプト エディション (VBScript) Visual Basicコードを使用してカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="78783-110">Forms containing form pages can be customized with code in Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="78783-111">フォーム定義と一緒に保存されるメッセージのサイズは、一般に大きいサイズです。</span><span class="sxs-lookup"><span data-stu-id="78783-111">Messages that are saved with form definitions are generally bigger in size.</span></span> <span data-ttu-id="78783-112">セキュリティとストレージ上の理由から、Outlook 2010 および Outlook 2013 では、任意のアイテムと一緒に保存されたフォーム定義は無視されます。</span><span class="sxs-lookup"><span data-stu-id="78783-112">For security and storage reasons, Outlook 2010 and Outlook 2013 ignore form definitions saved with any item.</span></span>
  
<span data-ttu-id="78783-113">カスタム フォーム定義と一緒に保存されたメッセージを 1 つの形式に変換するには、次の 4 つの名前付きプロパティを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="78783-113">To convert a message that is saved with a custom form definition to one without, you must remove four named properties:</span></span>
  
- [<span data-ttu-id="78783-114">PidLidFormStorage ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="78783-114">PidLidFormStorage Canonical Property</span></span>](pidlidformstorage-canonical-property.md)
    
- [<span data-ttu-id="78783-115">PidLidPageDirStream ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="78783-115">PidLidPageDirStream Canonical Property</span></span>](pidlidpagedirstream-canonical-property.md)
    
- [<span data-ttu-id="78783-116">PidLidFormPropStream ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="78783-116">PidLidFormPropStream Canonical Property</span></span>](pidlidformpropstream-canonical-property.md)
    
- [<span data-ttu-id="78783-117">PidLidScriptStream ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="78783-117">PidLidScriptStream Canonical Property</span></span>](pidlidscriptstream-canonical-property.md)
    
<span data-ttu-id="78783-118">さらに、そのメッセージに保存されたカスタム プロパティの定義を含む [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) 標準プロパティも削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="78783-118">In addition, you should also remove the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md) that contains the definitions of custom properties saved with that message.</span></span> <span data-ttu-id="78783-119">このプロパティを削除する副作用は、Outlook 2010 または Outlook 2013 オブジェクト モデルと Outlook 2010 または Outlook 2013 のユーザー インターフェイスがメッセージに設定されているユーザー プロパティにアクセスできなくなった点です。</span><span class="sxs-lookup"><span data-stu-id="78783-119">A side effect of removing this property is that the Outlook 2010 or Outlook 2013 object models and the Outlook 2010 or Outlook 2013 user interface will no longer be able to access user properties that have been set on the message.</span></span> <span data-ttu-id="78783-120">MAPI を使用してこれらのプロパティとその値にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="78783-120">You are still able to access these properties and their values through MAPI.</span></span> <span data-ttu-id="78783-121">このプロパティを削除しない場合、メッセージが別のフォーム定義で保存されている場合 [、PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) 標準プロパティは部分的に新しいデータで上書きされ、データの整合性は保証されません。</span><span class="sxs-lookup"><span data-stu-id="78783-121">Note that if you do not remove this property and the message is saved with another form definition, the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md) is partially overwritten with new data and data integrity is not guaranteed.</span></span> 
  
<span data-ttu-id="78783-122">[PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md)標準プロパティを削除する場合は [、PidLidCustomFlag](pidlidcustomflag-canonical-property.md)標準プロパティ **から INSP_PROPDEFINITION** フラグも削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="78783-122">If you remove the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md), then you should also remove the **INSP_PROPDEFINITION** flag from the [PidLidCustomFlag Canonical Property](pidlidcustomflag-canonical-property.md).</span></span>
  
<span data-ttu-id="78783-123">次の関数は、メッセージへのポインターを入力パラメーターとして受け入れ  `RemoveOneOff` [、PidLidPropertyDefinitionStream 標準プロパティ](pidlidpropertydefinitionstream-canonical-property.md)を削除するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="78783-123">The following function,  `RemoveOneOff`, accepts as input parameters a pointer to a message and an indicator whether to remove the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md).</span></span> <span data-ttu-id="78783-124">メッセージ ポインターを使用して [、IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) を呼び出して適切なプロパティ識別子を取得し [、IMAPIProp::D eleteProps](imapiprop-deleteprops.md) を呼び出して、名前付きプロパティを削除します。</span><span class="sxs-lookup"><span data-stu-id="78783-124">Using the message pointer, it calls [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the appropriate property identifiers, and then calls [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) to remove the named properties.</span></span> <span data-ttu-id="78783-125">また [、IMAPIProp::GetProps](imapiprop-getprops.md)を呼び出して [PidLidCustomFlag](pidlidcustomflag-canonical-property.md)標準プロパティを取得し、そのプロパティから必要に応じて **INSP \_ ONEOFFFLAGS** フラグと **INSP_PROPDEFINITION** フラグをクリアし、Outlook 2010 および Outlook 2013 が削除された名前付きプロパティを検索しません。</span><span class="sxs-lookup"><span data-stu-id="78783-125">It also calls [IMAPIProp::GetProps](imapiprop-getprops.md) to get the [PidLidCustomFlag Canonical Property](pidlidcustomflag-canonical-property.md) and clears the **INSP\_ONEOFFFLAGS** flag and **INSP_PROPDEFINITION** flag as appropriate from that property, so that Outlook 2010 and Outlook 2013 will not look for those named properties that have been removed.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="78783-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="78783-126">See also</span></span>

- [<span data-ttu-id="78783-127">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="78783-127">MAPI Constants</span></span>](mapi-constants.md)

