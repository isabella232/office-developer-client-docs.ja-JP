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
ms.openlocfilehash: a9f0fac76f06bd638aeff89ff096507209cc0287
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568456"
---
# <a name="iaddrbookgetdefaultdir"></a>IAddrBook::GetDefaultDir

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
初期のアドレス帳コンテナーのエントリの識別子を返します。
  
```cpp
HRESULT GetDefaultDir(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>パラメーター

 _lpcbEntryID_
  
> [out]_LppEntryID_パラメーターで指定されたエントリの識別子のバイト数へのポインター。 
    
 _lppEntryID_
  
> [out]既定のコンテナーのエントリの識別子へのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 既定のコンテナーのエントリ id が正常に返されました。
    
## <a name="remarks"></a>注釈

クライアント アプリケーションとサービス ・ プロバイダーは、既定のアドレス帳コンテナーのエントリの識別子を取得するために**GetDefaultDir**メソッドを呼び出します。 既定のコンテナーは、どのようなユーザーに表示されるアドレス帳を最初に開いたときに、アドレス帳に表示されます。 [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md)メソッドを呼び出すことで、既定のコンテナーが設定されていない場合は、MAPI は個人用アドレス帳 (PAB) ではない名前を持つ最初のコンテナーをデフォルトのコンテナーとして割り当てます。 このようなコンテナーが見つからない場合、個人用アドレス帳が既定のコンテナーになります。 
  
既定値を設定するのには、ディレクトリ、クライアント、またはプロバイダーは、 **SetDefaultDir**メソッドを呼び出します。 クライアントとプロバイダーは、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出すことはありません。アドレス帳への変更は処理されません、ため変更はすぐに反映されます。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenDefaultDir  <br/> |MFCMAPI では、 **GetDefaultDir**メソッドを使用して、既定のアドレス帳コンテナーの ID を取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[PidTagContainerFlags 標準プロパティ](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

