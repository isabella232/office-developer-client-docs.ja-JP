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
# <a name="remove-custom-form-definition-saved-with-a-message"></a>メッセージと共に保存されているユーザー設定フォーム定義を削除する
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックでは、ユーザー設定フォーム定義と共に保存されたメッセージを、フォーム定義なしで通常のメッセージに変換する C++ のコードサンプルを示します。
  
microsoft outlook 2010 または microsoft outlook 2013 では、ユーザー設定フォームページを含むフォームは、フォームライブラリに発行するか、または対応するフォーム定義をメッセージと共に保存することによって共有できます。 メッセージと共に保存されるユーザー設定フォームは、"one-off フォーム" と呼ばれることがあります。このフォームは、1回限りのインスタンスとして特定のメッセージを表示するためにのみ共有されるためです。 通常、フォームがフォームライブラリに発行されていないが、受信者がアイテムを開くときにユーザー設定フォームを使用する必要がある場合です。 フォームデザイナーでフォームを one-off として指定するには、フォームの [**プロパティ**] ページで、[**アイテムと共にフォーム定義を送信**する] チェックボックスをオンにします。 
  
フォームページを含むフォームは、Visual Basic Scripting Edition (VBScript) のコードを使用してカスタマイズできます。 フォーム定義と共に保存されるメッセージは、通常、サイズが大きくなります。 セキュリティとストレージの理由により、outlook 2010 および outlook 2013 では、アイテムと共に保存されるフォーム定義は無視されます。
  
ユーザー設定フォーム定義に保存されているメッセージをに変換せずに変換するには、次の4つの名前付きプロパティを削除する必要があります。
  
- [PidLidFormStorage ���K���̃v���p�e�B](pidlidformstorage-canonical-property.md)
    
- [PidLidPageDirStream ���K���̃v���p�e�B](pidlidpagedirstream-canonical-property.md)
    
- [PidLidFormPropStream ���K���̃v���p�e�B](pidlidformpropstream-canonical-property.md)
    
- [PidLidScriptStream ���K���̃v���p�e�B](pidlidscriptstream-canonical-property.md)
    
さらに、そのメッセージと共に保存されたカスタムプロパティの定義を含む[PidLidPropertyDefinitionStream 標準プロパティ](pidlidpropertydefinitionstream-canonical-property.md)も削除する必要があります。 このプロパティを削除すると、outlook 2010 または outlook 2013 オブジェクトモデルと outlook 2010 または outlook 2013 ユーザーインターフェイスは、メッセージに設定されたユーザープロパティにアクセスできなくなります。 MAPI を使用してこれらのプロパティとそれらの値にアクセスすることはできます。 このプロパティを削除しないで、メッセージを別のフォーム定義で保存した場合、 [PidLidPropertyDefinitionStream 標準プロパティ](pidlidpropertydefinitionstream-canonical-property.md)は新しいデータで上書きされ、データの整合性は保証されないことに注意してください。 
  
[PidLidPropertyDefinitionStream 標準プロパティ](pidlidpropertydefinitionstream-canonical-property.md)を削除した場合は、 [PidLidCustomFlag 標準プロパティ](pidlidcustomflag-canonical-property.md)から**INSP_PROPDEFINITION**フラグも削除する必要があります。
  
次の関数`RemoveOneOff`は、メッセージへのポインターと、 [PidLidPropertyDefinitionStream 標準プロパティ](pidlidpropertydefinitionstream-canonical-property.md)を削除するかどうかを示す、入力パラメーターとして受け入れます。 メッセージポインターを使用して、 [imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)を呼び出して適切なプロパティ識別子を取得し、次に[imapiprop::D eleteprops](imapiprop-deleteprops.md)を呼び出して名前付きプロパティを削除します。 また、 [imapiprop:: GetProps](imapiprop-getprops.md)を呼び出して[PidLidCustomFlag 標準プロパティ](pidlidcustomflag-canonical-property.md)を取得し、そのプロパティから必要に応じて**insp\_oneoffflags**フラグと**INSP_PROPDEFINITION**フラグをクリアします。そのため、Outlook 2010 およびOutlook 2013 は、削除された名前付きプロパティを検索しません。 
  
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

