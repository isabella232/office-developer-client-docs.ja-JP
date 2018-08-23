---
title: ACCELERATEABSDI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ACCELERATEABSDI
api_type:
- HeaderDef
ms.assetid: da67dcf4-1411-4fc9-992c-115485019bd3
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 101e74f3e35e3664dd29e59f166b2f0af6e1dcba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592039"
---
# <a name="accelerateabsdi"></a>ACCELERATEABSDI
 
**適用されます**: Outlook 2013 |Outlook 2016 
  
モードレスのアドレス帳のダイアログ ボックスのアクセラレータ キーを処理するコールバック関数を定義します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|によって実装される関数の定義:  <br/> |MAPI  <br/> |
|によって呼び出される関数を定義します。  <br/> |クライアント アプリケーション  <br/> |
   
```cpp
BOOL (STDMETHODCALLTYPE ACCELERATEABSDI)( 
  ULONG_PTR ulUIParam,
  LPVOID lpvmsg
);
```

## <a name="parameters"></a>パラメーター

 _ulUIParam_
  
> [in]ユーザー インターフェイスの情報を関数に渡すために使用される実装固有の値です。 Microsoft Windows で実行中のアプリケーションで_ulUIParam_ ] ダイアログ ボックスの親ウィンドウ ハンドルは、され型の HWND の**ULONG_PTR**にキャストします。 0 の値は、親ウィンドウがないことを示します。 
    
 _lpvmsg_
  
> [in]Windows メッセージへのポインター。
    
## <a name="return-value"></a>戻り値

**ACCELERATEABSDI**のプロトタイプを持つ関数は、メッセージを処理する場合に TRUE を返します。 
  
## <a name="remarks"></a>注釈

**ACCELERATEABSDI**のプロトタイプでは関数は、クライアント アプリケーションが、 _ulFlags_ 、 [ADRPARM](adrparm.md)構造体のメンバーで、DIALOG_SDI フラグを設定する場合にのみは、モードレス ダイアログ ボックスでのみ使用します。 
  
モードレス ダイアログ ボックスでは、独自のループではなく、クライアント アプリケーションの Windows メッセージ ループを共有します。 アプリケーション メッセージ ループを制御するには、CTRL キーを押しながら P キーを押すなど印刷用のアクセラレータ キー、 **ACCELERATEABSDI**を呼び出すため、ダイアログの使用に基づいて関数をテストし、動作にどのようなアクセラレータ キーを認識しません。 
  
クライアントのメッセージ ループの呼び出し**ACCELERATEABSDI**は、クライアントが[IAddrBook::Address](iaddrbook-address.md)メソッドを使用して、モードレスのアドレス帳] ダイアログ ボックスを呼び出したときに関数を基づいています。 MAPI は、 [DISMISSMODELESS](dismissmodeless.md)関数のプロトタイプでは関数を呼び出すと、この呼び出しが終了します。 
  

