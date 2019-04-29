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
  
[モードレスアドレス帳] ダイアログボックスで、アクセラレータキーを処理するためのコールバック関数を定義します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|定義された関数の実装:  <br/> |MAPI  <br/> |
|によって呼び出された定義済み関数:  <br/> |クライアント アプリケーション  <br/> |
   
```cpp
BOOL (STDMETHODCALLTYPE ACCELERATEABSDI)( 
  ULONG_PTR ulUIParam,
  LPVOID lpvmsg
);
```

## <a name="parameters"></a>パラメーター

 _uluiparam_
  
> 順番ユーザーインターフェイス情報を関数に渡すために使用される実装固有の値。 Microsoft Windows 上で実行されているアプリケーションでは、 _uluiparam_はダイアログボックスの親ウィンドウハンドルで、 **ULONG_PTR**にキャストする型 HWND です。 値が0の場合は、親ウィンドウがないことを示します。 
    
 _lpvmsg_
  
> 順番Windows メッセージへのポインター。
    
## <a name="return-value"></a>戻り値

**ACCELERATEABSDI**プロトタイプを使用している関数は、メッセージを処理する場合は TRUE を返します。 
  
## <a name="remarks"></a>注釈

**ACCELERATEABSDI**プロトタイプに基づく関数は、モードレスダイアログでのみ使用されます。つまり、クライアントアプリケーションが[ADRPARM](adrparm.md)構造の_ulflags_メンバーで DIALOG_SDI フラグを設定している場合に限られます。 
  
モードレスダイアログは、独自のループを持たずに、クライアントアプリケーションの Windows メッセージループを共有します。 メッセージループを制御するアプリケーションでは、ダイアログで使用されるアクセラレータキーがわからないため、 **ACCELERATEABSDI**ベースの関数を呼び出して、CTRL + P などのアクセラレータキーをテストし、操作することができます。 
  
クライアントのメッセージループは、 [IAddrBook:: address](iaddrbook-address.md)メソッドを使用して、モードレスアドレス帳ダイアログボックスを呼び出したときに**ACCELERATEABSDI**ベースの関数を呼び出します。 この呼び出しは、MAPI が[DISMISSMODELESS](dismissmodeless.md)関数プロトタイプに基づいて関数を呼び出したときに終了します。 
  

