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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d9ad74d8ae02a49ee3c222394caedfd571f84b1c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436875"
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
  
> [out]  _lppEntryID_ パラメーターが指すエントリ識別子内のバイト 数へのポインター。 
    
 _lppEntryID_
  
> [out]既定のコンテナーのエントリ識別子へのポインターを指すポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 既定のコンテナーのエントリ識別子が正常に返されました。
    
## <a name="remarks"></a>注釈

クライアント アプリケーションとサービス プロバイダーは **、GetDefaultDir** メソッドを呼び出して、既定のアドレス帳コンテナーのエントリ識別子を取得します。 既定のコンテナーは、ユーザーがアドレス帳を最初に開いたときにアドレス帳に表示されるコンテナーです。 [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md)メソッドの呼び出しによって既定のコンテナーが設定されていない場合、MAPI は、個人アドレス帳 (PAB) ではない名前を持つ最初のコンテナーを既定のコンテナーとして割り当てる。 そのようなコンテナーが見つからない場合、PAB は既定のコンテナーになります。 
  
既定のディレクトリを設定するには、クライアントまたはプロバイダーが **SetDefaultDir メソッドを呼び出** します。 クライアントとプロバイダーは [、IMAPIProp::SaveChanges メソッドを呼び出す必要](imapiprop-savechanges.md) があります。アドレス帳に対する変更は処理されないので、変更は直ちに永続的に行います。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenDefaultDir  <br/> |MFCMAPI は **GetDefaultDir** メソッドを使用して、既定のアドレス帳コンテナーの ID を取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[PidTagContainerFlags 標準プロパティ](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

