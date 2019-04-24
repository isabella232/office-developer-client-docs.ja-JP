---
title: IMAPITableSeekRowApprox
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SeekRowApprox
api_type:
- COM
ms.assetid: ce5e8c43-06af-4afc-9138-5cc51d8fc401
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: bbb79097d03a8ea09cb4aff374231ee780e15395
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328841"
---
# <a name="imapitableseekrowapprox"></a>IMAPITable::SeekRowApprox

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブル内のおおよその分数位置にカーソルを移動します。 
  
```cpp
HRESULT SeekRowApprox(
ULONG ulNumerator,
ULONG ulDenominator
);
```

## <a name="parameters"></a>パラメーター

 _ulnumerator_
  
> 順番テーブルの位置を表す分数の分子へのポインター。 _ulnumerator_パラメーターが0の場合、カーソルは分母値に関係なく、テーブルの先頭に配置されます。 _ulnumerator_が_ulnumerator_パラメーターと等しい場合、カーソルは最後の表の行の後に配置されます。 
    
 _uldenominator_
  
> 順番テーブルの位置を表す分数の分母へのポインター。 _uldenominator_パラメーターを0にすることはできません。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> シーク操作が正常に完了しました。
    
MAPI_E_BUSY 
  
> 別の操作が進行中であるため、行のシーク操作を開始できません。 進行中の操作が完了することを許可するか、停止する必要があります。
    
## <a name="remarks"></a>解説

**IMAPITable:: seekrowapprox**メソッドを呼び出した後のテーブル内のカーソルの位置は、分母がヒューリスティックで、正確ではない可能性があります。 たとえば、特定のプロバイダーでは、パフォーマンス上の理由からツリーの最上位として表の中間点を処理して、バイナリツリーの上にテーブルを実装する場合があります。 ツリーが分散されていない場合、使用される中間点は、テーブルを正確に半分になることはありません。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

スクロールバーの実装のデータを提供するために、 **seekrowapprox**を呼び出します。 たとえば、ユーザーがスクロールボックスをスクロールバーの下に移動した場合は、 **seekrowapprox**呼び出し、 _ulnumerator_と_ulnumerator_を使用して同等の小数点以下の値を渡すことによって、そのアクションをモデル化することができます。 **seekrowapprox** search は、常にテーブルの先頭からの絶対パスです。 テーブルの末尾に移動するには、 _ulnumerator_と_ulnumerator_の値が同じである必要があります。 
  
適切な番号スキームを使用してください。 つまり、テーブルの途中で位置をシークするには、1/2、10/20、または50/100 を指定できます。 
  
## <a name="see-also"></a>関連項目



[IMAPITable : IUnknown](imapitableiunknown.md)

