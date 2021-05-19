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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 29677ce74f405e8ca03f1639f3d98288532e9653
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424617"
---
# <a name="iaddrbooksetpab"></a>IAddrBook::SetPAB

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
特定のコンテナーを個人用アドレス帳 (PAB) として指定します。
  
```cpp
HRESULT SetPAB(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>パラメーター

 _cbEntryID_
  
> [in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。 
    
 _lpEntryID_
  
> [in]PAB として指定するコンテナーのエントリ識別子へのポインター。 _lpEntryID_ パラメーターは NULL にすることはできません。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 指定したコンテナーが PAB として確立されています。
    
## <a name="remarks"></a>注釈

クライアントとサービス プロバイダーは **SetPAB** メソッドを呼び出して、特定のコンテナーを PAB として指定します。 PAB は、他のコンテナーからコピーされたエントリと新しいエントリで構成されるコンテナーです。 
  
**SetPAB** の呼び出しは、そのコンテナーが使用不能になるまで、または **SetPAB** への後続の呼び出しを通じて新しいコンテナーが PAB になるまで、コンテナーを PAB として確立します。 
  
クライアントとプロバイダーは、PAB の変更を永続的に行うために [IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドを呼び出す必要があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|AbContDlg.cpp  <br/> |CAbContDlg::OnSetPAB  <br/> |MFCMAPI は **SetPAB** メソッドを使用して、指定したコンテナーを PAB にします。  <br/> |
   
## <a name="see-also"></a>関連項目



[IAddrBook::GetPAB](iaddrbook-getpab.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[PidTagContainerFlags 標準プロパティ](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

