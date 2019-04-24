---
title: iaddrbookgetpab
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6c565c088fd4ef7d5df141bf770c560f79535998
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349302"
---
# <a name="iaddrbookgetpab"></a>IAddrBook::GetPAB

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
個人用アドレス帳 (PAB) として指定されているコンテナーのエントリ識別子を返します。
  
```cpp
HRESULT GetPAB(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>パラメーター

 _lpcbEntryID_
  
> 読み上げ_lppentryid_パラメーターによって指定されたエントリ識別子のバイト数へのポインター。 
    
 _lppentryid_
  
> 読み上げPAB のエントリ識別子へのポインターへのポインター。 PAB として指定されているコンテナーがない場合、 _lppentryid_パラメーターには0が格納されます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> PAB のエントリ識別子が正常に返されました。
    
## <a name="remarks"></a>解説

クライアントは、 **getpab**メソッドを呼び出して、pab として指定されたコンテナーのエントリ識別子を取得します。 pab がプロファイルで確立されていない場合、MAPI は、変更を許可するアドレス帳階層の最初のコンテナーを pab として選択します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|maindlg .cpp  <br/> |CMainDlg:: onopenpab  <br/> |mfcmapi は、 **getpab**メソッドを使用して、ユーザーの個人用アドレス帳の ID を取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[PidTagContainerFlags 標準プロパティ](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

