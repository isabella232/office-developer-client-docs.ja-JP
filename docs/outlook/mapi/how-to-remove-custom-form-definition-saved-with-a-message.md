---
title: メッセージと共に保存されているユーザー設定フォーム定義を削除する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 6a270f0c-104a-84a1-9adf-aea166f89071
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: 737b04a8899a03931c98067909dce2ad2f47a339
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564275"
---
# <a name="remove-custom-form-definition-saved-with-a-message"></a>メッセージと共に保存されているユーザー設定フォーム定義を削除する
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックでは、カスタム フォーム定義で保存されたメッセージを、フォーム定義なしで通常のメッセージに変換する C++ のコード サンプルを示します。
  
ユーザー Microsoft Outlook 2010またはMicrosoft Outlook 2013、カスタム フォーム ページを含むフォームを共有するには、カスタム フォーム ページをフォーム ライブラリに発行するか、対応するフォーム定義をメッセージで保存します。 メッセージと一緒に保存されたカスタム フォームは、その特定のメッセージを 1 回限りインスタンスとして表示するためにのみ共有されるので、一般に"1 回限りフォーム" と呼ばれます。 通常、フォームがフォーム ライブラリで発行されていないが、アイテムを開く際に受信者がカスタム フォームを使用する場合にこれを行います。 フォームの [プロパティ] ページの [アイテムを使用してフォーム定義を送信する] チェック ボックスをオンにすると、フォームがフォーム デザイナーで 1 回切り替えで指定できます。 
  
フォーム ページを含むフォームは、スクリプト エディション (VBScript) Visual Basicコードを使用してカスタマイズできます。 フォーム定義と一緒に保存されるメッセージのサイズは、一般に大きいサイズです。 セキュリティとストレージ上の理由から、Outlook 2010 および Outlook 2013 では、任意のアイテムと一緒に保存されたフォーム定義は無視されます。
  
カスタム フォーム定義と一緒に保存されたメッセージを 1 つの形式に変換するには、次の 4 つの名前付きプロパティを削除する必要があります。
  
- [PidLidFormStorage ���K���̃v���p�e�B](pidlidformstorage-canonical-property.md)
    
- [PidLidPageDirStream ���K���̃v���p�e�B](pidlidpagedirstream-canonical-property.md)
    
- [PidLidFormPropStream ���K���̃v���p�e�B](pidlidformpropstream-canonical-property.md)
    
- [PidLidScriptStream ���K���̃v���p�e�B](pidlidscriptstream-canonical-property.md)
    
さらに、そのメッセージに保存されたカスタム プロパティの定義を含む [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) 標準プロパティも削除する必要があります。 このプロパティを削除する副作用は、Outlook 2010 または Outlook 2013 オブジェクト モデルと Outlook 2010 または Outlook 2013 のユーザー インターフェイスがメッセージに設定されているユーザー プロパティにアクセスできなくなった点です。 MAPI を使用してこれらのプロパティとその値にアクセスできます。 このプロパティを削除しない場合、メッセージが別のフォーム定義で保存されている場合 [、PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) 標準プロパティは部分的に新しいデータで上書きされ、データの整合性は保証されません。 
  
[PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md)標準プロパティを削除する場合は [、PidLidCustomFlag](pidlidcustomflag-canonical-property.md)標準プロパティ **から INSP_PROPDEFINITION** フラグも削除する必要があります。
  
次の関数は、メッセージへのポインターを入力パラメーターとして受け入れ  `RemoveOneOff` [、PidLidPropertyDefinitionStream 標準プロパティ](pidlidpropertydefinitionstream-canonical-property.md)を削除するかどうかを示します。 メッセージ ポインターを使用して [、IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) を呼び出して適切なプロパティ識別子を取得し [、IMAPIProp::D eleteProps](imapiprop-deleteprops.md) を呼び出して、名前付きプロパティを削除します。 また [、IMAPIProp::GetProps](imapiprop-getprops.md)を呼び出して [PidLidCustomFlag](pidlidcustomflag-canonical-property.md)標準プロパティを取得し、そのプロパティから必要に応じて **INSP \_ ONEOFFFLAGS** フラグと **INSP_PROPDEFINITION** フラグをクリアし、Outlook 2010 および Outlook 2013 が削除された名前付きプロパティを検索しません。 
  
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

## <a name="see-also"></a>関連項目

- [MAPI 定数](mapi-constants.md)

