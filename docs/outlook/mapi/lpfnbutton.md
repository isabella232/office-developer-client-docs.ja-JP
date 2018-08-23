---
title: LPFNBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.LPFNBUTTON
api_type:
- COM
ms.assetid: cb91ae1d-1ea8-4f02-a1f1-f2a356a71477
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e1f15a5f031f5c5a9568b8a36722eaac011b814c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801279"
---
# <a name="lpfnbutton"></a>LPFNBUTTON

  
  
**適用対象**: Outlook 
  
MAPI が、アドレス帳] ダイアログ ボックスで、オプション ボタン コントロールをアクティブにするために呼び出すコールバック関数を定義します。 このボタンは、通常、**詳細**ボタンです。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|によって実装される関数の定義:  <br/> |サービス プロバイダー  <br/> |
|によって呼び出される関数を定義します。  <br/> |MAPI  <br/> |
   
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
  
> [in]すべてのダイアログ ボックスの親ウィンドウまたはこの関数を表示するウィンドウのハンドルです。
    
 _lpvContext_
  
> [in]任意の値へのポインターは、MAPI では、それを呼び出すときに、コールバック関数に渡されます。 この値は、クライアント アプリケーションにとって意味のアドレスを表すことができます。 通常、C++ コードでは、 _lpvContext_のポインターを表します C++ オブジェクトにします。 
    
 _cbEntryID_
  
> [in]_LpSelection_パラメーターで指定されたエントリの識別子のバイト単位のサイズです。 
    
 _lpSelection_
  
> [in]ダイアログ ボックスで選択範囲を定義するエントリの識別子へのポインター。
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>����

クライアント アプリケーションでは、[詳細] ダイアログ ボックスのボタンを定義するのには**LPFNBUTTON**プロトタイプに基づいてコールバック関数を呼び出します。 クライアントは、 [IAddrBook::Details](iaddrbook-details.md)メソッドの呼び出しでコールバック関数へのポインターを渡します。 
  
サービス プロバイダーでは、[詳細] ダイアログ ボックスのボタンを定義するのには**LPFNBUTTON**のプロトタイプのフック関数を呼び出します。 プロバイダーは、 [IMAPISupport::Details](imapisupport-details.md)メソッドの呼び出しでは、このフック関数へのポインターを渡します。 
  
どちらの場合も、ダイアログ ボックスが表示され、定義済みのボタンを選択した場合、MAPI は**LPFNBUTTON**を呼び出します。 
  
## <a name="see-also"></a>関連項目



[BuildDisplayTable](builddisplaytable.md)

