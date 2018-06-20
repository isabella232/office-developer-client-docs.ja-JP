---
title: IAddrBookGetPAB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetPAB
api_type:
- COM
ms.assetid: 9830e09c-700f-469b-a54d-4e4e0583aa84
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 3d67d71effde87711e3be9aca1b979627acda37d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800389"
---
# <a name="iaddrbookgetpab"></a>られたユーザーのプライマリ

  
  
**適用されます**: Outlook 
  
個人用アドレス帳 (PAB) として指定されているコンテナーのエントリの識別子を返します。
  
```cpp
HRESULT GetPAB(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Parameters

 _lpcbEntryID_
  
> [out]_LppEntryID_パラメーターで指定されたエントリの識別子のバイト数へのポインター。 
    
 _lppEntryID_
  
> [out]個人アドレス帳のエントリの識別子へのポインターへのポインター。 _LppEntryID_パラメーターには、コンテナーが、個人用アドレス帳として指定されてない場合は 0 が含まれています。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 個人アドレス帳のエントリ id が正常に返されました。
    
## <a name="remarks"></a>備考

クライアントは、個人用アドレス帳として指定されているコンテナーのエントリの識別子を取得するために**GetPAB**メソッドを呼び出します。 場合は、プロファイルに個人用アドレス帳が確立されていない、MAPI、個人用アドレス帳として最初のコンテナーの選択、アドレス帳階層の変更を可能にします。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenPAB  <br/> |MFCMAPI では、 **GetPAB**メソッドを使用して、ユーザーの個人用アドレス帳の ID を取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[PidTagContainerFlags の標準的なプロパティ](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook: IMAPIProp](iaddrbookimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

