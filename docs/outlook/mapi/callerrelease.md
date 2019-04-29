---
title: CALLERRELEASE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CALLERRELEASE
api_type:
- HeaderDef
ms.assetid: 80ba893d-3380-4db1-9175-f5b84cb57def
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9a22550e60c9de38236a9f612c7e60f50f18978f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408727"
---
# <a name="callerrelease"></a>CALLERRELEASE

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブルビューが解放されているときに、テーブルデータオブジェクトを解放できるコールバック関数を定義します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|定義された関数の実装:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
|によって呼び出された定義済み関数:  <br/> |MAPI  <br/> |
   
```cpp
void CALLERRELEASE(
  ULONG_PTR ulCallerData,
  LPTABLEDATA lpTblData,
  LPMAPITABLE lpVue
);
```

## <a name="parameters"></a>パラメーター

 _ulcallerdata_
  
> 順番MAPI によってテーブルビューで保存され、 **callerrelease**ベースのコールバック関数に渡される発信者データ。 このデータは、リリースされるテーブルビューに関するコンテキストを提供します。 
    
 _lpTblData_
  
> 順番[itabledata](itabledataiunknown.md)へのポインター: 解放されるテーブルビューの基になるテーブルデータオブジェクトの IUnknown インターフェイス。 
    
 _lpvue_
  
> 順番リリースされるテーブルビューの[IMAPITable: IUnknown](imapitableiunknown.md)インターフェイスへのポインター。 これは、解放するオブジェクトを作成した[itabledata:: hrgetview](itabledata-hrgetview.md)メソッドの_lppMAPITable_パラメーターで返される table オブジェクトのインターフェイスです。 
    
## <a name="return-value"></a>戻り値

なし 
  
## <a name="remarks"></a>注釈

テーブルデータオブジェクトを設定したクライアントアプリケーションまたはサービスプロバイダーは、 [itabledata:: hrgetview](itabledata-hrgetview.md)を呼び出して、読み取り専用で並べ替えられたテーブルのビューを作成できます。 **hrgetview**の呼び出しでは、 **callerrelease**ベースのコールバック関数へのポインターが渡されます。また、テーブルビューと共に保存されるコンテキストもあります。 テーブルビューの参照カウントが0に戻り、ビューが解放されるとき、 **IMAPITable**実装はコールバック関数を呼び出し、 _ulcallerdata_パラメーターにコンテキストを渡します。 
  
**callerrelease**ベースのコールバック関数の一般的な使用方法は、基になるテーブルのデータオブジェクトを解放することで、以降の処理中にそのオブジェクトを追跡する必要はありません。 
  

