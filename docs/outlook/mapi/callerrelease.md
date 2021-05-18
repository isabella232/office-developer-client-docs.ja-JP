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
  
テーブル ビューのリリース時にテーブル データ オブジェクトを解放できるコールバック関数を定義します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|定義された関数は、次の方法で実装されます。  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
|によって呼び出される定義済み関数:  <br/> |MAPI  <br/> |
   
```cpp
void CALLERRELEASE(
  ULONG_PTR ulCallerData,
  LPTABLEDATA lpTblData,
  LPMAPITABLE lpVue
);
```

## <a name="parameters"></a>パラメーター

 _ulCallerData_
  
> [in]テーブル ビューを使用して MAPI によって保存され **、CALLERRELEASE** ベースのコールバック関数に渡される呼び出し元データ。 データは、リリースされるテーブル ビューに関するコンテキストを提供します。 
    
 _lpTblData_
  
> [in] [ITableData へのポインター: 解放](itabledataiunknown.md) されるテーブル ビューの基になるテーブル データ オブジェクトの IUnknown インターフェイス。 
    
 _lpVue_
  
> [in] [IMAPITable へのポインター: 解放されるテーブル ビューの IUnknown](imapitableiunknown.md) インターフェイス。 これは、解放するオブジェクトを作成した [ITableData::HrGetView](itabledata-hrgetview.md)メソッドの _lppMAPITable_ パラメーターで返されるテーブル オブジェクトのインターフェイスです。 
    
## <a name="return-value"></a>戻り値

なし 
  
## <a name="remarks"></a>注釈

テーブル データ オブジェクトを設定したクライアント アプリケーションまたはサービス プロバイダーは [、ITableData::HrGetView](itabledata-hrgetview.md) を呼び出して、テーブルの読み取り専用で並べ替えたビューを作成できます。 **HrGetView の呼び** 出しは **、CALLERRELEASE** ベースのコールバック関数へのポインターと、テーブル ビューに保存されるコンテキストを渡します。 テーブル ビューの参照カウントが 0 に戻り、ビューが解放されると **、IMAPITable** 実装はコールバック関数を呼び出し  _、ulCallerData_ パラメーターでコンテキストを渡します。 
  
**CALLERRELEASE** ベースのコールバック関数の一般的な使用は、基になるテーブル データ オブジェクトを解放し、後続の処理中に追跡する必要はありません。 
  

