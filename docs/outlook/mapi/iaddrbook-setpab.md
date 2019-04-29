---
title: iaddrbooksetpab
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
  
> 順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。 
    
 _lて tryid_
  
> 順番PAB として指定するコンテナーのエントリ id へのポインター。 _lな tryid_パラメーターを NULL にすることはできません。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 指定したコンテナーは PAB として確立されています。
    
## <a name="remarks"></a>注釈

クライアントおよびサービスプロバイダーは、 **setpab**メソッドを呼び出して、特定のコンテナーを PAB として指定します。 PAB は、他のコンテナーからコピーしたエントリと、新しいエントリで構成されるコンテナーです。 
  
**setpab**の呼び出しによって、コンテナーが pab として設定され、そのコンテナーが使用できなくなるか、またはその後の**setpab**への呼び出しによって新しいコンテナーが pab になります。 
  
クライアントとプロバイダーは、PAB を永続的に変更するために[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出す必要はありません。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|abdlg  <br/> |cabコンテ dlg:: OnSetPAB  <br/> |mfcmapi は、 **setpab**メソッドを使用して、指定されたコンテナーを PAB に設定します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IAddrBook::GetPAB](iaddrbook-getpab.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[PidTagContainerFlags 標準プロパティ](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

