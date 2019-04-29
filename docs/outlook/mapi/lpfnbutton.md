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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 804bd23a148b942fd4580d1e3465fc1f65ff5978
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431513"
---
# <a name="lpfnbutton"></a>LPFNBUTTON

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[アドレス帳] ダイアログボックスでオプションのボタンコントロールをアクティブ化するために MAPI が呼び出すコールバック関数を定義します。 通常、このボタンは [**詳細**] ボタンです。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|定義された関数の実装:  <br/> |サービス プロバイダー  <br/> |
|によって呼び出された定義済み関数:  <br/> |MAPI  <br/> |
   
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

 _uluiparam_
  
> 順番この関数が表示する、任意のダイアログボックスまたはウィンドウの親ウィンドウのハンドル。
    
 _lpvcontext_
  
> 順番MAPI がコールバック関数に渡す任意の値へのポインター。 この値は、クライアントアプリケーションにとって重要なアドレスを表すことができます。 通常、c++ コードでは、 _lpvcontext_は c++ オブジェクトへのポインターを表します。 
    
 _cbEntryID_
  
> 順番_lpselection_パラメーターで指定されたエントリ識別子のサイズ (バイト単位)。 
    
 _lpselection_
  
> 順番ダイアログボックスの選択範囲を定義するエントリ識別子へのポインター。
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

クライアントアプリケーションは、 **LPFNBUTTON**プロトタイプに基づいてコールバック関数を呼び出し、[詳細] ダイアログボックスにボタンを定義します。 クライアントは、 [IAddrBook::D etails](iaddrbook-details.md)メソッドへの呼び出しで、コールバック関数へのポインターを渡します。 
  
サービスプロバイダーは、 **LPFNBUTTON**プロトタイプに基づいて、[詳細] ダイアログボックスにボタンを定義するためのフック関数を呼び出します。 プロバイダーは、 [imapisupport::D etails](imapisupport-details.md)メソッドへの呼び出しで、このフック関数へのポインターを渡します。 
  
どちらの場合も、ダイアログボックスが表示され、ユーザーが [定義済み] ボタンを選択すると、MAPI は**LPFNBUTTON**を呼び出します。 
  
## <a name="see-also"></a>関連項目



[BuildDisplayTable](builddisplaytable.md)

