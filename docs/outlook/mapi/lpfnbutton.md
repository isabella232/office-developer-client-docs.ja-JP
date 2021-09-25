---
title: LPFNBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.LPFNBUTTON
api_type:
- COM
ms.assetid: cb91ae1d-1ea8-4f02-a1f1-f2a356a71477
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 05cce66e06e32162abf6f3183ed9c7b94d24e9b7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556211"
---
# <a name="lpfnbutton"></a>LPFNBUTTON

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アドレス帳ダイアログ ボックスでオプションのボタン コントロールをアクティブ化するために MAPI が呼び出すコールバック関数を定義します。 通常、このボタンは [詳細] **ボタン** です。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|定義された関数は、次の方法で実装されます。  <br/> |サービス プロバイダー  <br/> |
|によって呼び出される定義済み関数:  <br/> |MAPI  <br/> |
   
```cpp
SCODE (STDMETHODCALLTYPE FAR * LPFNBUTTON)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext,
  ULONG cbEntryID,
  LPENTRYID lpSelection,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _ulUIParam_
  
> [in]この関数が表示するダイアログ ボックスまたはウィンドウの親ウィンドウのハンドル。
    
 _lpvContext_
  
> [in]MAPI がコールバック関数を呼び出す際にコールバック関数に渡される任意の値へのポインター。 この値は、クライアント アプリケーションにとって重要なアドレスを表します。 通常、C++ コードの場合  _、lpvContext_ は C++ オブジェクトへのポインターを表します。 
    
 _cbEntryID_
  
> [in]  _lpSelection_ パラメーターが指すエントリ識別子のサイズ (バイト単位)。 
    
 _lpSelection_
  
> [in]ダイアログ ボックスで選択範囲を定義するエントリ識別子へのポインター。
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

クライアント アプリケーションは、詳細ダイアログ ボックスでボタンを定義するために **、LPFNBUTTON** プロトタイプに基づいてコールバック関数を呼び出します。 クライアントは [、IAddrBook::D etails](iaddrbook-details.md) メソッドの呼び出しでコールバック関数へのポインターを渡します。 
  
サービス プロバイダーは、詳細ダイアログ ボックスでボタンを定義するために **、LPFNBUTTON** プロトタイプに基づいてフック関数を呼び出します。 プロバイダーは [、IMAPISupport::D etails](imapisupport-details.md) メソッドの呼び出しで、このフック関数へのポインターを渡します。 
  
どちらの場合も、ダイアログ ボックスが表示され、ユーザーが定義されたボタンを選択すると、MAPI は **LPFNBUTTON を呼び出します**。 
  
## <a name="see-also"></a>関連項目



[BuildDisplayTable](builddisplaytable.md)

