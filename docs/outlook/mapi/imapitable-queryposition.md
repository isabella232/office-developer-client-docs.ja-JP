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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 502bc24ece37c91e2cac23cf8486df96d5a71377
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584339"
---
# <a name="imapitablequeryposition"></a>IMAPITable::QueryPosition

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
小数部の値に基づいて、カーソルの現在のテーブルの行位置を取得します。
  
```cpp
HRESULT QueryPosition(
ULONG FAR * lpulRow,
ULONG FAR * lpulNumerator,
ULONG FAR * lpulDenominator
);
```

## <a name="parameters"></a>パラメーター

 _lpulRow_
  
> [out]現在の行の行番号へのポインター。 行番号は 0 から始まります。テーブルの最初の行は 0 です。 
    
 _lpulNumerator_
  
> [out]テーブルの位置を識別する分数の分子の部分へのポインター。
    
 _lpulDenominator_
  
> [out]テーブルの位置を識別する分数の分母となるへのポインター。 _LpulDenominator_パラメーターは、ゼロにすることはできません。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> メソッドでは、 _lpulRow_、 _lpulNumerator_、 _lpulDenominator_で有効な値が返されます。
    
## <a name="remarks"></a>注釈

**IMAPITable::QueryPosition**メソッドは、現在の行位置を指定し、現在の行とテーブルの末尾には、相対的な位置を示す小数部の値の番号の両方を返します。 MAPI は、読み取られる次の行として、現在の行を定義します。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

_LpulDenominator_パラメーターのテーブルの行の正確な数を取得する必要はありません。概算値となります。 
  
、現在の行を特定できない場合は、 _lpulRow_に 0 xffffffff の値を返します。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**QueryPosition**を使用すると、スクロール バーのスクロール ボックスを配置します。 100 行を含むテーブルでの**QueryPosition**は、 _lpulDenominator_パラメーターに 100、75、 _lpulRow_パラメーターで、 _lpulNumerator_パラメーターで 75 の値を返す場合は、スクロール ボックス 3/4 を配置することスクロール バーの間での方法です。 
  
テーブル内の行の数をされている_lpulDenominator_の値に依存しません。 **QueryPosition**は、正確な行にカーソルが配置されていることを常に識別できません。 
  
**QueryPosition**への呼び出しには、大量メモリ、特に大規模な分類されたテーブルにはが含まれます。 _LpulRow_パラメーターは、0 xffffffff に設定されている場合、大量のメモリは**QueryPosition**を現在の行を特定するために必要でした。 _LpulNumerator_および_lpulDenominator_パラメーターで指定された行にテーブルを配置する[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)メソッドを呼び出します。 ただし、常にされないように**QueryPosition**がメモリが倍にしていない場合、同じ行を現在の位置として確立するために**SeekRowApprox** 。 
  
## <a name="see-also"></a>関連項目



[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

