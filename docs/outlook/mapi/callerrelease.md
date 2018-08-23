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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 69ee06ef8c8f5499dec41232d3dc7b374b15a744
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799747"
---
# <a name="callerrelease"></a>CALLERRELEASE

  
  
**適用対象**: Outlook 
  
テーブル ビューがリリースされたとき、テーブルのデータ オブジェクトをリリースできるコールバック関数を定義します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装される関数の定義:  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
|によって呼び出される関数を定義します。  <br/> |MAPI  <br/> |
   
```cpp
void CALLERRELEASE(
  ULONG_PTR ulCallerData,
  LPTABLEDATA lpTblData,
  LPMAPITABLE lpVue
);
```

## <a name="parameters"></a>パラメーター

 _ulCallerData_
  
> [in]コールバック関数を表形式ビューで、MAPI によって保存され、 **CALLERRELEASE**に渡される呼び出し元のデータに基づいています。 データでは、リリースされている表形式のビューのコンテキストを提供します。 
    
 _lpTblData_
  
> [in]ポインター、 [ITableData: IUnknown](itabledataiunknown.md)リリースされている表形式のビューの基になるテーブルのデータ オブジェクトのインターフェイスです。 
    
 _lpVue_
  
> [in]ポインター、 [IMAPITable: IUnknown](imapitableiunknown.md)リリースされている表形式のビューのインターフェイスです。 これは、リリースするオブジェクトを作成した[ITableData::HrGetView](itabledata-hrgetview.md)メソッドの_lppMAPITable_パラメーターで返される table オブジェクトのインターフェイスです。 
    
## <a name="return-value"></a>戻り値

なし 
  
## <a name="remarks"></a>注釈

クライアント アプリケーションまたはサービス プロバイダーのテーブルのデータ オブジェクトにデータを設定するには、読み取り専用で、並べ替えられたテーブルのビューを作成する[ITableData::HrGetView](itabledata-hrgetview.md)を呼び出すことができます。 **HrGetView**への呼び出しは、 **CALLERRELEASE**ベースのコールバック関数とテーブル ・ ビューを保存するコンテキストへのポインターを渡します。 テーブル ビューの参照カウントがゼロに戻ります、ビューがリリースされている、 **IMAPITable**実装は、コンテキストを_ulCallerData_パラメーターに渡して、コールバック関数を呼び出します。 
  
**CALLERRELEASE**ベースのコールバック関数の一般的な用途では、基になるテーブルのデータ オブジェクトを解放していないを追跡するため、後続の処理中にします。 
  

