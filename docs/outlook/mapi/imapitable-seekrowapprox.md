---
title: IMAPITableSeekRowApprox
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.SeekRowApprox
api_type:
- COM
ms.assetid: ce5e8c43-06af-4afc-9138-5cc51d8fc401
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b88e7d71639d880a001a48d60e6089e9358f807a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592313"
---
# <a name="imapitableseekrowapprox"></a>IMAPITable::SeekRowApprox

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
カーソルをテーブル内のおおよその小数位置に移動します。 
  
```cpp
HRESULT SeekRowApprox(
ULONG ulNumerator,
ULONG ulDenominator
);
```

## <a name="parameters"></a>パラメーター

 _ulNumerator_
  
> [in]表の位置を表す分数の分子へのポインター。 _ulNumerator パラメーターが 0_ の場合、分母の値に関係なく、カーソルはテーブルの先頭に配置されます。 _ulNumerator が_ _ulDenominator_ パラメーターと等しい場合、カーソルは最後のテーブル行の後に配置されます。 
    
 _ulDenominator_
  
> [in]表の位置を表す分数の分母へのポインター。 _ulDenominator パラメーター_ は 0 にすることはできません。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> シーク操作が成功しました。
    
MAPI_E_BUSY 
  
> 行シーク操作が開始されるのを防ぐ別の操作が進行中です。 進行中の操作の完了を許可するか、停止する必要があります。
    
## <a name="remarks"></a>注釈

**IMAPITable::SeekRowApprox** メソッドの呼び出し後のテーブル内のカーソル位置は、ヒューリスティックに分数であり、正確ではない可能性があります。 たとえば、特定のプロバイダーはバイナリ ツリーの上にテーブルを実装し、パフォーマンス上の理由からテーブルの中途半端な位置をツリーの上端として扱う場合があります。 ツリーのバランスが取されていない場合、使用される中途半端なポイントがテーブルの正確な途中ではない可能性があります。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**SeekRowApprox を呼び** 出して、スクロール バーの実装のデータを提供します。 たとえば、スクロール ボックスをスクロール バーの 2/3 下に配置する場合は **、SeekRowApprox** を呼び出し  _、ulNumerator_ と  _ulDenominator_ を使用して同等の小数部の値を渡すことによって、そのアクションをモデル化できます。 **SeekRowApprox 検索** は、常にテーブルの先頭から絶対値です。 表の末尾に移動するには  _、ulNumerator_ と  _ulDenominator_ の値が同じである必要があります。 
  
適切な番号スキームを使用します。 つまり、テーブルの途中の位置をシークするには、1/2、10/20、または 50/100 を指定できます。 
  
## <a name="see-also"></a>関連項目



[IMAPITable : IUnknown](imapitableiunknown.md)

