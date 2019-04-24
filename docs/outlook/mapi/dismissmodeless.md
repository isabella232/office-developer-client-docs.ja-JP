---
title: DISMISSMODELESS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DISMISSMODELESS
api_type:
- COM
ms.assetid: ef93ef3d-c159-40ae-9b8d-0af8a0567565
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: dd962515a85cb6a4b8661a0fd5294cea55cd6e96
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339775"
---
# <a name="dismissmodeless"></a>DISMISSMODELESS

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
モードレスアドレス帳ダイアログボックスが閉じられたときに MAPI が呼び出すコールバック関数を定義します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|定義された関数の実装:  <br/> |クライアント アプリケーション  <br/> |
|によって呼び出された定義済み関数:  <br/> |MAPI  <br/> |
   
```cpp
void (STDMETHODCALLTYPE DISMISSMODELESS)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext
);
```

## <a name="parameters"></a>パラメーター

 _uluiparam_
  
> 順番通常、ユーザーインターフェイス情報を関数に渡すために使用される実装固有の値。 たとえば、Microsoft Windows では、このパラメーターはダイアログボックスの親ウィンドウハンドルで、型は HWND で、 **ULONG_PTR**にキャストされます。 値が0の場合は、親ウィンドウがないことを示します。 
    
 _lpvcontext_
  
> 順番MAPI がコールバック関数に渡す任意の値へのポインター。 この値は、クライアントアプリケーションにとって重要なアドレスを表すことができます。 通常、c++ コードでは、 _lpvcontext_は c++ オブジェクトインスタンスのアドレスへのポインターです。 
    
## <a name="return-value"></a>戻り値

なし
  
## <a name="remarks"></a>解説

クライアントアプリケーションは、モードレスアドレス帳ダイアログボックスを起動するときに、 [ACCELERATEABSDI](accelerateabsdi.md)プロトタイプに基づいて関数への呼び出しを Windows メッセージループに含めます。このメソッドは、アクセラレータキーをチェックして処理します。 ダイアログボックスが閉じられると、MAPI は**DISMISSMODELESS**ベースの関数を呼び出して、クライアントアプリケーションが**ACCELERATEABSDI**ベースの関数の呼び出しを停止するようにします。 
  
## <a name="see-also"></a>関連項目



[ADRPARM](adrparm.md)

