---
title: DISMISSMODELESS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.DISMISSMODELESS
api_type:
- COM
ms.assetid: ef93ef3d-c159-40ae-9b8d-0af8a0567565
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: bc1921f1761754cab47ec1b478957bffbad63119
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556785"
---
# <a name="dismissmodeless"></a>DISMISSMODELESS

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
モードレス アドレス帳ダイアログ ボックスを閉じ、MAPI が呼び出すコールバック関数を定義します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|定義された関数は、次の方法で実装されます。  <br/> |クライアント アプリケーション  <br/> |
|によって呼び出される定義済み関数:  <br/> |MAPI  <br/> |
   
```cpp
void (STDMETHODCALLTYPE DISMISSMODELESS)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext
);
```

## <a name="parameters"></a>パラメーター

 _ulUIParam_
  
> [in]実装固有の値は、通常、ユーザー インターフェイス情報を関数に渡す場合に使用します。 たとえば、Microsoft Windowsでは、このパラメーターはダイアログ ボックスの親ウィンドウ ハンドルであり、HWND 型で、ダイアログ ボックスにキャスト **ULONG_PTR。** 値が 0 の場合は、親ウィンドウが表示されません。 
    
 _lpvContext_
  
> [in]MAPI がコールバック関数を呼び出す際にコールバック関数に渡される任意の値へのポインター。 この値は、クライアント アプリケーションにとって重要なアドレスを表します。 通常、C++ コードの  _場合、lpvContext_ は C++ オブジェクト インスタンスのアドレスへのポインターです。 
    
## <a name="return-value"></a>戻り値

なし
  
## <a name="remarks"></a>注釈

クライアント アプリケーションがモードレス アドレス帳ダイアログ ボックスを呼び出すと、アクセラレータ キーをチェックして処理する[ACCELERATEABSDI](accelerateabsdi.md)プロトタイプに基づく関数の呼び出しが Windows メッセージ ループに含まれます。 ダイアログ ボックスが閉じられると、MAPI は **DISMISSMODELESS** ベースの関数を呼び出して、クライアント アプリケーションが **ACCELERATEABSDI** ベースの関数の呼び出しを停止します。 
  
## <a name="see-also"></a>関連項目



[ADRPARM](adrparm.md)

