---
title: IAddrBookSetPAB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetPAB
api_type:
- COM
ms.assetid: 75daf9d4-6975-435f-91e5-1b41e0047ab7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 461b59ff4f4c8a93f3a9945b05e31aef9a2997bf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569303"
---
# <a name="iaddrbooksetpab"></a>IAddrBook::SetPAB

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
個人用アドレス帳 (PAB) には、特定のコンテナーを指定します。
  
```cpp
HRESULT SetPAB(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>パラメーター

 _cbEntryID_
  
> [in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。 
    
 _lpEntryID_
  
> [in]個人アドレス帳として指定するコンテナーのエントリの識別子へのポインター。 _LpEntryID_パラメーターは、NULL にすることはできません。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 指定したコンテナーは、個人用アドレス帳として確立されています。
    
## <a name="remarks"></a>注釈

クライアントとサービス ・ プロバイダーとして、個人用アドレス帳の特定のコンテナーを指定するのには**SetPAB**メソッドを呼び出します。 個人アドレス帳は、他のコンテナーと同様に新しいエントリからコピーしたエントリで構成されるコンテナーです。 
  
**SetPAB**への呼び出しは、そのコンテナーが使用できなくなった、または、 **SetPAB**への後続の呼び出しで個人用アドレス帳を新しいコンテナーになりますまで、個人用アドレス帳としてコンテナーを確立します。 
  
クライアントとプロバイダーがありませんに個人用アドレス帳の変更を永続的な[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|AbContDlg.cpp  <br/> |CAbContDlg::OnSetPAB  <br/> |MFCMAPI では、 **SetPAB**メソッドを使用して、指定したコンテナーに、個人用アドレス帳を作成します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IAddrBook::GetPAB](iaddrbook-getpab.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[PidTagContainerFlags 標準プロパティ](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

