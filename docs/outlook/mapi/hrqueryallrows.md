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
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
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
  
> [in]行を取得する MAPI テーブルへのポインター。 
    
 _ptaga_
  
> [in]テーブル列を示すプロパティ タグの配列を含む [SPropTagArray](sproptagarray.md) 構造体へのポインター。 これらのタグは、取得する特定の列を選択するために使用されます。 _ptaga パラメーターが_ NULL の場合 **、HrQueryAllRows は** _ptable_ パラメーターで渡された現在のテーブル ビューの列セット全体を取得します。 
    
 _pres_
  
> [in]取得の [制限を含む SRestriction](srestriction.md) 構造体へのポインター。 _pres パラメーターが_ NULL の場合 **、HrQueryAllRows は** 制限を行います。 
    
 _psos_
  
> [in]取得する列の並べ替え順序を識別する [SSortOrderSet](ssortorderset.md) 構造体へのポインター。 _psos パラメーターが_ NULL の場合、テーブルの既定の並べ替え順序が使用されます。 
    
 _crowsMax_
  
> [in]取得する行の最大数。 _crowsMax_ パラメーターの値が 0 の場合、取得される行数に制限はありません。 
    
 _pprows_
  
> [out]取得したテーブル行へのポインターの配列を含む、返される [SRowSet](srowset.md) 構造体へのポインターへのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しは、テーブルの予想される行を取得しました。 
    
MAPI_E_TABLE_TOO_BIG 
  
> テーブル内の行数は  _、crowsMax_ パラメーターに渡される数よりも大きくなります。 
    
## <a name="remarks"></a>注釈

クライアント アプリケーションまたはサービス プロバイダーは、pres パラメーターによって指される制限を課す以外に **、HrQueryAllRows** が取得しようとする行数を  _制御_ できません。 _crowsMax_ パラメーターは、取得を特定の数のテーブル行に制限するのではなく、取得された行を保持するために使用できる最大メモリ量を定義します。 大量のメモリ オーバーフローに対する唯一の保護は  _、crowsMax_ を設定することで提供される stopgap 機能です。 エラーが返MAPI_E_TABLE_TOO_BIGテーブルに含まれる行が多すぎて、メモリ内で一度に保持される行が多すぎます。 
  
通常、メッセージ ストア テーブルやプロバイダー テーブルなど、小さいテーブルは **、通常、HrQueryAllRows** を使用して安全に取得できます。 コンテンツ テーブルや受信者テーブルなど、非常に大きい可能性があるテーブルは [、IMAPITable::QueryRows](imapitable-queryrows.md) メソッドを使用してサブセクションで走査する必要があります。 
  
**HrQueryAllRows** が呼び出された場合、テーブルプロパティが未定義の場合、テーブルプロパティの種類とプロパティPT_NULLプロパティ識別子が返PROP_ID_NULL 
  

