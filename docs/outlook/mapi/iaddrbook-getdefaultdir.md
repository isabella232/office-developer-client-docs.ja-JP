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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 7309f65965fe3c88f927eeba0bbcccff97c479af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800383"
---
# <a name="iaddrbookgetdefaultdir"></a>IAddrBook::GetDefaultDir

  
  
**適用されます**: Outlook 
  
初期のアドレス帳コンテナーのエントリの識別子を返します。
  
```cpp
HRESULT GetDefaultDir(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Parameters

 _lpcbEntryID_
  
> [out]_LppEntryID_パラメーターで指定されたエントリの識別子のバイト数へのポインター。 
    
 _lppEntryID_
  
> [out]既定のコンテナーのエントリの識別子へのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 既定のコンテナーのエントリ id が正常に返されました。
    
## <a name="remarks"></a>備考

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
  
[PidTagContainerFlags の標準的なプロパティ](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook: IMAPIProp](iaddrbookimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

