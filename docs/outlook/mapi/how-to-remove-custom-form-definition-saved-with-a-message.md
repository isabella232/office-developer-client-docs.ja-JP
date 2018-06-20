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
# <a name="remove-custom-form-definition-saved-with-a-message"></a>ユーザー設定のフォーム定義を保存し、メッセージを削除します。
  
**適用されます**: Outlook 
  
このトピックでは、フォーム定義を含まない通常のメッセージにユーザー設定のフォーム定義に保存されているメッセージに変換する C++ のコード例を示します。
  
Microsoft Outlook 2010 または Microsoft Outlook 2013 では、フォーム ライブラリに発行すること、または、メッセージに対応するフォーム定義を保存してユーザー設定フォームのページを含むフォームを共有できます。 メッセージと共に保存されるカスタム フォームが一般的と呼ばれる「one-off フォーム、」1 回限りのインスタンスとその特定のメッセージを表示するだけのフォームを共有するため。 通常これを行うフォームをフォーム ライブラリに発行されませんが、受信者がアイテムを開くときにユーザー設定フォームを使用するとします。 フォームは、フォームの [**プロパティ**] ページで [**アイテムのフォーム レイアウトも送信**] チェック ボックスを選択して one-off フォーム デザイナーで指定できます。 
  
フォーム ページを含むフォームをカスタマイズするには、Visual Basic Scripting Edition (VBScript) 内のコードとします。 フォーム定義が保存されているメッセージは、一般的にサイズが大きくします。 セキュリティおよびストレージ上の理由から、Outlook 2010、Outlook 2013 は、フォーム定義がアイテムと共に保存を無視します。
  
ないユーザー設定のフォーム定義に保存されているメッセージを変換するには、4 つの名前付きプロパティを削除する必要があります。
  
- [PidLidFormStorage ���K���̃v���p�e�B](pidlidformstorage-canonical-property.md)
    
- [PidLidPageDirStream ���K���̃v���p�e�B](pidlidpagedirstream-canonical-property.md)
    
- [PidLidFormPropStream ���K���̃v���p�e�B](pidlidformpropstream-canonical-property.md)
    
- [PidLidScriptStream ���K���̃v���p�e�B](pidlidscriptstream-canonical-property.md)
    
さらに、そのメッセージを保存するカスタム プロパティの定義が含まれています[PidLidPropertyDefinitionStream の標準的なプロパティ](pidlidpropertydefinitionstream-canonical-property.md)を削除することもする必要があります。 このプロパティを削除することの副次的な影響を Outlook 2010 または Outlook 2013 オブジェクト モデルは、Outlook 2010 または Outlook 2013 のユーザー インターフェイスは、メッセージに設定されているユーザー プロパティにアクセスすることができなきます。 まだ MAPI を介してこれらのプロパティとその値にアクセスできます。 このプロパティを削除しないし、別のフォーム定義を使用してメッセージを保存、 [PidLidPropertyDefinitionStream の標準的なプロパティ](pidlidpropertydefinitionstream-canonical-property.md)は、部分的に新しいデータで上書きに注意してくださいし、データの整合性は保証されません。 
  
[PidLidPropertyDefinitionStream の標準的なプロパティ](pidlidpropertydefinitionstream-canonical-property.md)を削除する場合、 [PidLidCustomFlag の標準的なプロパティ](pidlidcustomflag-canonical-property.md)から**INSP_PROPDEFINITION**フラグも削除必要があります。
  
次の関数では、 `RemoveOneOff`、受け入れる入力パラメーターとしてメッセージとインジケーターへのポインター、 [PidLidPropertyDefinitionStream の標準的なプロパティ](pidlidpropertydefinitionstream-canonical-property.md)を削除するかどうか。 メッセージ ポインターを使用して、適切なプロパティの識別子を取得する[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を呼び出す、名前付きプロパティを削除するのには[IMAPIProp::DeleteProps](imapiprop-deleteprops.md)を呼び出します。 また[PidLidCustomFlag の標準的なプロパティ](pidlidcustomflag-canonical-property.md)を取得する[IMAPIProp::GetProps](imapiprop-getprops.md)を呼び出すし、クリア、 **INSP\_ONEOFFFLAGS**フラグは、 **INSP_PROPDEFINITION**としてフラグを設定、そのプロパティの適切なので、Outlook 2010 と削除されたこれらの名前付きプロパティの outlook 2013 を検索しません。 
  
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

- [MAPI �萔](mapi-constants.md)

