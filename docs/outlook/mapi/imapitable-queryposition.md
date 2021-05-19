---
title: IMAPITableQueryPosition
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QueryPosition
api_type:
- COM
ms.assetid: 510b2e21-ba27-47dd-87cb-2a549e31fa28
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2e44d824bbb5cc96c51d7ca91eb639001bc52a71
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415664"
---
# <a name="imapitablequeryposition"></a>IMAPITable::QueryPosition

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
小数部の値に基づいて、カーソルの現在のテーブル行の位置を取得します。
  
```cpp
HRESULT QueryPosition(
ULONG FAR * lpulRow,
ULONG FAR * lpulNumerator,
ULONG FAR * lpulDenominator
);
```

## <a name="parameters"></a>パラメーター

 _lpulRow_
  
> [out]現在の行の番号へのポインター。 行番号は 0 から始ります。テーブルの最初の行は 0 です。 
    
 _lpulNumerator_
  
> [out]表の位置を識別する分数の分子へのポインター。
    
 _lpulDenominator_
  
> [out]テーブル位置を識別する分数の分母へのポインター。 _lpulDenominator パラメーター_ は 0 にすることはできません。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> メソッドは  _、lpulRow_  _、lpulNumerator、および_  _lpulDenominator で有効な値を返しました_。
    
## <a name="remarks"></a>注釈

**IMAPITable::QueryPosition** メソッドは、現在の行の位置を決定し、現在の行の番号と、テーブルの末尾への相対位置を示す小数部の値の両方を返します。 MAPI は、現在の行を読み取る次の行として定義します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

_lpulDenominator_ パラメーターのテーブル内の行の正確な数を返す必要があります。近似値を指定できます。 
  
現在の行を特定できない場合は  _、lpulRow_ の値0xFFFFFFFF返します。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

QueryPosition を **使用すると** 、スクロール バーにスクロール ボックスを配置できます。 たとえば、100 行を含むテーブルで **、QueryPosition** が _lpulNumerator_ パラメーターで 75、lpulDenominator パラメーターで 100、lpulRow パラメーターに75 の値を返す場合、スクロール バーを横切る方向のスクロール ボックス 3/4 を配置できます。 
  
_lpulDenominator_ の値がテーブル内の行数に依存しない。 **QueryPosition** では、カーソルが配置されている正確な行を常に特定できません。 
  
QueryPosition の呼 **び出** しには、特に大きな分類テーブルに対して大量のメモリが含まれる場合があります。 _lpulRow パラメーターが_ 現在の行に設定されている **0xFFFFFFFF、QueryPosition** で現在の行を決定するために必要なメモリが多すぎます。 [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)メソッドを呼び出して _、lpulNumerator_ パラメーターと _lpulDenominator_ パラメーターで識別される行にテーブルを配置します。 ただし、メモリが要因ではない場合 **、SeekRowApprox** が現在の位置と同じ行 **QueryPosition** として確立されるとは限らない。 
  
## <a name="see-also"></a>関連項目



[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

