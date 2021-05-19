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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 46e87caa68a45a188272340db408c52546f02a57
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420375"
---
# <a name="accelerateabsdi"></a>ACCELERATEABSDI
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
モードレス アドレス帳ダイアログ ボックスでアクセラレータ キーを処理するコールバック関数を定義します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|定義された関数は、次の方法で実装されます。  <br/> |MAPI  <br/> |
|によって呼び出される定義済み関数:  <br/> |クライアント アプリケーション  <br/> |
   
```cpp
BOOL (STDMETHODCALLTYPE ACCELERATEABSDI)( 
  ULONG_PTR ulUIParam,
  LPVOID lpvmsg
);
```

## <a name="parameters"></a>パラメーター

 _ulUIParam_
  
> [in]ユーザー インターフェイス情報を関数に渡す場合に使用される実装固有の値。 Microsoft Windows で実行されているアプリケーションでは _、ulUIParam_ はダイアログ ボックスの親ウィンドウ ハンドルであり、HWND 型で、ULONG_PTR に **キャストされます**。 値が 0 の場合は、親ウィンドウが表示されません。 
    
 _lpvmsg_
  
> [in]メッセージへのポインター Windowsします。
    
## <a name="return-value"></a>戻り値

**ACCELERATEABSDI プロトタイプを持つ** 関数は、メッセージを処理する場合は TRUE を返します。 
  
## <a name="remarks"></a>注釈

**ACCELERATEABSDI** プロトタイプに基づく関数は、モードレス ダイアログでのみ使用されます。つまり、クライアント アプリケーションが [ADRPARM](adrparm.md)構造体の _ulFlags_ メンバーで DIALOG_SDI フラグを設定している場合のみです。 
  
モードレス ダイアログは、独自のループをWindows、クライアント アプリケーションのメッセージ ループを共有します。 メッセージ ループを制御するアプリケーションは、ダイアログで使用するアクセラレータ キーを知らないので **、ACCELERATEABSDI** ベースの関数を呼び出して、印刷用の Ctrl + P などのアクセラレータ キーをテストして処理します。 
  
クライアントのメッセージ ループは、クライアントが [IAddrBook::Address](iaddrbook-address.md)メソッドを使用してモードレス アドレス帳ダイアログ ボックスを呼び出すと **、ACCELERATEABSDI** ベースの関数を呼び出します。 この呼び出しは、MAPI が DISMISSMODELESS 関数プロトタイプに基づいて関数 [を呼び出す場合に](dismissmodeless.md) 終了します。 
  

