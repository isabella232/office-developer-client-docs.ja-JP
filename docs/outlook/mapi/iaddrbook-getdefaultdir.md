---
title: IAddrBookGetDefaultDir
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetDefaultDir
api_type:
- COM
ms.assetid: 7a9fdf3f-fd76-40fb-8217-967c6efba5f6
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d9ad74d8ae02a49ee3c222394caedfd571f84b1c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336695"
---
# <a name="iaddrbookgetdefaultdir"></a>IAddrBook::GetDefaultDir

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
最初のアドレス帳コンテナーのエントリ識別子を返します。
  
```cpp
HRESULT GetDefaultDir(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>パラメーター

 _lpcbEntryID_
  
> 読み上げ_lppentryid_パラメーターによって指定されたエントリ識別子のバイト数へのポインター。 
    
 _lppentryid_
  
> 読み上げ既定のコンテナーのエントリ識別子へのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 既定のコンテナーのエントリ識別子が正常に返されました。
    
## <a name="remarks"></a>解説

クライアントアプリケーションおよびサービスプロバイダーは、 **GetDefaultDir**メソッドを呼び出して、既定のアドレス帳コンテナーのエントリ識別子を取得します。 既定のコンテナーは、アドレス帳が最初に開かれたときに、ユーザーにアドレス帳で表示されることを示します。 [IAddrBook:: SetDefaultDir](iaddrbook-setdefaultdir.md)メソッドの呼び出しによって既定のコンテナーが設定されていない場合、MAPI は、個人用アドレス帳 (PAB) ではない名前の最初のコンテナーを既定のコンテナーとして割り当てます。 このようなコンテナーが見つからない場合、PAB は既定のコンテナーになります。 
  
既定のディレクトリを設定するために、クライアントまたはプロバイダーは**SetDefaultDir**メソッドを呼び出します。 クライアントとプロバイダーは、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出す必要はありません。アドレス帳への変更は処理されないため、変更はすぐに永続的に加えられます。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|maindlg .cpp  <br/> |CMainDlg:: OnOpenDefaultDir  <br/> |mfcmapi は、 **GetDefaultDir**メソッドを使用して、既定のアドレス帳コンテナーの ID を取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[PidTagContainerFlags 標準プロパティ](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

