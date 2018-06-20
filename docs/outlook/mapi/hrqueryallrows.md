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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 5c62e5919c6e605aa4b60f48072996ed1fd4c355
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800317"
---
# <a name="hrqueryallrows"></a>HrQueryAllRows

  
  
**適用されます**: Outlook 
  
テーブルのすべての行を取得します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
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

## <a name="parameters"></a>Parameters

 _参照を必要_
  
> [in]行の取得元の MAPI テーブルへのポインター。 
    
 _ptaga_
  
> [in]プロパティの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインターでは、テーブルの列を示すタグ付けします。 これらのタグを使用して、取得する特定の列を選択します。 _Ptaga_パラメーターが NULL の場合は、 **HrQueryAllRows**は、全体の列のセット_の参照を必要_パラメーターで渡された現在のテーブル ビューを取得します。 
    
 _プレス_
  
> [in]取得の制限を含む[SRestriction](srestriction.md)構造体へのポインター。 _プレス_パラメーターが NULL の場合は、 **HrQueryAllRows**には制限がありません。 
    
 _pso_
  
> [in]取得する列の並べ替え順序を識別する[SSortOrderSet](ssortorderset.md)構造体へのポインター。 _Pso_のパラメーターが NULL の場合は、テーブルの既定の並べ替え順序が使用されます。 
    
 _crowsMax_
  
> [in]取得する行の最大数。 _CrowsMax_パラメーターの値が 0 の場合は、取得される行の数に制限は設定されていません。 
    
 _pprows_
  
> [out]取得したテーブルの行へのポインターの配列を格納する返される[SRowSet](srowset.md)構造体へのポインターへのポインター。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 呼び出しには、予想されるテーブルの行が取得されます。 
    
MAPI_E_TABLE_TOO_BIG 
  
> テーブル内の行の数は、 _crowsMax_パラメーターに渡された値よりも大きくなります。 
    
## <a name="remarks"></a>備考

クライアント アプリケーションまたはサービス プロバイダーには、 **HrQueryAllRows**を取得しよう、制限を課すことによって指す_プレス_パラメーター以外の行の数を制御がありません。 _CrowsMax_パラメーターは、テーブルのロー数を取得を制限することはできませんではなく取得したすべての行を保持するために使用できるメモリの最大量を定義します。 大容量のメモリのオーバーフローに対する唯一の防策は、 _crowsMax_を設定することによって提供される暫定的な機能です。 エラーの戻り値が MAPI_E_TABLE_TOO_BIG では、テーブルには、すべてを一度にメモリに保持するが多すぎる行が含まれています。 
  
メッセージ ストアのテーブルや、プロバイダーのテーブルなど、通常は小さいテーブル通常安全に取得できる**HrQueryAllRows**とします。 [IMAPITable::QueryRows](imapitable-queryrows.md)メソッドを使用してのサブセクションでは、テーブルの内容のテーブルなど、宛先テーブルも非常に大きな危険にさらさを走査する必要があります。 
  
プロパティ タイプ PT_NULL および PROP_ID_NULL プロパティの識別子を持つ場合は、テーブルのプロパティに定義された**HrQueryAllRows**が呼び出されたときに、返されます 
  

