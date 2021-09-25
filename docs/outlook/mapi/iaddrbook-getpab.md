---
title: IAddrBookGetPAB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBook.GetPAB
api_type:
- COM
ms.assetid: 9830e09c-700f-469b-a54d-4e4e0583aa84
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: be1858d1a0e9eb0fe6743fd3d91c533408161d12
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571851"
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
  
> [out]  _lppEntryID_ パラメーターが指すエントリ識別子内のバイト 数へのポインター。 
    
 _lppEntryID_
  
> [out]PAB のエントリ識別子へのポインター。 コンテナーが PAB として指定されていない場合  _、lppEntryID_ パラメーターには 0 が含まれる。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> PAB のエントリ識別子が正常に返されました。
    
## <a name="remarks"></a>注釈

クライアントは **GetPAB メソッドを呼** び出して、PAB として指定されたコンテナーのエントリ識別子を取得します。 PAB がプロファイルに確立されていない場合、MAPI は変更を許可するアドレス帳階層の最初のコンテナーとして PAB として選択します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenPAB  <br/> |MFCMAPI は **GetPAB** メソッドを使用して、ユーザーの個人用アドレス帳の ID を取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[PidTagContainerFlags 標準プロパティ](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

