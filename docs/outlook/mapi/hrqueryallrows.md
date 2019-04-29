---
title: HrQueryAllRows
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrQueryAllRows
api_type:
- HeaderDef
ms.assetid: b08fadcf-cdf3-48b7-9489-d7f745266482
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0f09304f21180d9ebc2a1e1dcc54ebadd3622804
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422895"
---
# <a name="hrqueryallrows"></a>HrQueryAllRows

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブルのすべての行を取得します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
HRESULT HrQueryAllRows(
  LPMAPITABLE ptable,
  LPSPropTagArray ptaga,
  LPSRestriction pres,
  LPSSortOrderSet psos,
  LONG crowsMax,
  LPSRowSet FAR * pprows
);
```

## <a name="parameters"></a>パラメーター

 _ptable_
  
> 順番行を取得する MAPI テーブルへのポインター。 
    
 _ptaga_
  
> 順番表の列を示すプロパティタグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。 これらのタグは、取得する特定の列を選択するために使用されます。 _ptaga_パラメーターが NULL の場合、 **hrqueryallrows**は、 _ptable_パラメーターで渡された現在のテーブルビューの列セット全体を取得します。 
    
 _感情_
  
> 順番取得制限を含む[srestriction](srestriction.md)構造体へのポインター。 _プレゼン_パラメーターが NULL の場合、 **hrqueryallrows**は制限を行いません。 
    
 _pso_
  
> 順番取得する列の並べ替え順序を識別する[ssortorderset](ssortorderset.md)構造体へのポインター。 _pso_パラメーターが NULL の場合は、テーブルの既定の並べ替え順序が使用されます。 
    
 _crowsMax_
  
> 順番取得する行の最大数。 _crowsMax_パラメーターの値が0の場合、取得される行の数に制限は設定されません。 
    
 _pprows_
  
> 読み上げ取得したテーブルの行へのポインターの配列を含む、返された[rowset](srowset.md)構造体へのポインターへのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しは、テーブルの予測された行を取得しています。 
    
MAPI_E_TABLE_TOO_BIG 
  
> テーブル内の行数が、 _crowsMax_パラメーターに渡された数値よりも大きくなっています。 
    
## <a name="remarks"></a>注釈

クライアントアプリケーションまたはサービスプロバイダーは、"終了" パラメーターで指定された制限を課すのではなく、 **hrqueryallrows**が取得し__ ようとしている行の数を制御できません。 _crowsMax_パラメーターでは、取得を特定の数のテーブル行に制限せずに、取得したすべての行の保持に使用できるメモリの最大量を定義します。 大規模メモリオーバーフローに対する保護は、 _crowsMax_を設定することによって提供される stopgap 機能です。 error return MAPI_E_TABLE_TOO_BIG は、テーブルに含まれる行が多すぎて、一度にすべてのメモリに保持されていないことを意味します。 
  
通常、メッセージストアテーブルやプロバイダーテーブルなどの小さなテーブルは、通常**hrqueryallrows**を使用して安全に取得できます。 contents [:: QueryRows](imapitable-queryrows.md)メソッドを使用して、コンテンツテーブルや受信者テーブルなど、非常に大きなテーブルがサブセクションでトラバースされる可能性があります。 
  
**hrqueryallrows**が呼び出されたときにテーブルのプロパティが未定義になっている場合は、プロパティの種類が PT_NULL およびプロパティ識別子の PROP_ID_NULL で返されます。 
  

