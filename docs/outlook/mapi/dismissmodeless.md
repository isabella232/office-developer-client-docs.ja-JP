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
ms.openlocfilehash: dc830665f425b747d2fdb05641dc037a2e84f695
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799941"
---
# <a name="dismissmodeless"></a>DISMISSMODELESS

  
  
**適用対象**: Outlook 
  
モードレスのアドレス帳のダイアログ ボックスを閉じるにはときに、MAPI が呼び出すコールバック関数を定義します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|によって実装される関数の定義:  <br/> |クライアント アプリケーション  <br/> |
|によって呼び出される関数を定義します。  <br/> |MAPI  <br/> |
   
```cpp
void (STDMETHODCALLTYPE DISMISSMODELESS)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext
);
```

## <a name="parameters"></a>パラメーター

 _ulUIParam_
  
> [in]ユーザー インターフェイスの情報を関数に渡すために使用される通常の実装に固有の値です。 などの Microsoft Windows でこのパラメーター] ダイアログ ボックスの親ウィンドウ ハンドル、キャスト、 **ULONG_PTR**型 HWND の。 0 の値は、親ウィンドウがないことを示します。 
    
 _lpvContext_
  
> [in]任意の値へのポインターは、MAPI では、それを呼び出すときに、コールバック関数に渡されます。 この値は、クライアント アプリケーションにとって意味のアドレスを表すことができます。 通常、C++ コードでは、 _lpvContext_は、C++ オブジェクトのインスタンスのアドレスへのポインターです。 
    
## <a name="return-value"></a>戻り値

なし
  
## <a name="remarks"></a>注釈

モードレスのアドレス帳のダイアログ ボックスを呼び出すと、クライアント アプリケーションが含まれます Windows メッセージ ループで[ACCELERATEABSDI](accelerateabsdi.md)のプロトタイプをチェックし、アクセラレータ キーを処理するには関数の呼び出しには。 ダイアログ ボックスが閉じられると、 **DISMISSMODELESS**ベースの関数**ACCELERATEABSDI**を呼び出すクライアント アプリケーションを停止するため、MAPI 呼び出しは、関数を基づいています。 
  
## <a name="see-also"></a>関連項目



[ADRPARM](adrparm.md)

