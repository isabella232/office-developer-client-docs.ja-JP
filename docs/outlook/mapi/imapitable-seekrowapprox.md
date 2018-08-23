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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e6803c54ddd60c1bcebbe7a139c2edf2e7f4449d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572092"
---
# <a name="imapitableseekrowapprox"></a>IMAPITable::SeekRowApprox

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
テーブルのおおよその小数部から成る位置にカーソルを移動します。 
  
```cpp
HRESULT SeekRowApprox(
ULONG ulNumerator,
ULONG ulDenominator
);
```

## <a name="parameters"></a>パラメーター

 _ulNumerator_
  
> [in]テーブルの位置を表す分数の分子へのポインター。 _UlNumerator_パラメーターが 0 の場合は、分母の値に関係なく、テーブルの先頭にカーソルが配置されます。 _UlNumerator_が_ulDenominator_のパラメーターと等しい場合は、カーソルはテーブルの最後の行の後です。 
    
 _ulDenominator_
  
> [in]テーブルの位置を表す分数の分母となるへのポインター。 _UlDenominator_パラメーターは、ゼロにすることはできません。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> シーク操作が正常に完了しました。
    
MAPI_E_BUSY 
  
> 別の操作は、シーク操作の開始行を防止する処理中です。 実行中の操作を完了できるか、それを停止する必要があります。
    
## <a name="remarks"></a>注釈

**IMAPITable::SeekRowApprox**メソッドを呼び出した後、テーブルのカーソル位置は、ヒューリスティックによって、正確なことができない場合があります分数です。 たとえば、特定のプロバイダーを実装バイナリ ツリーは、上にテーブル パフォーマンス上の理由から、ツリーの最上部にテーブルの中間点を扱うこと。 ツリーのバランスがとれていない場合、使用される中間点があります、表の途中で正確に。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

スクロール バーの実装にデータを提供する**SeekRowApprox**を呼び出します。 などの場合は、スクロール ボックス 2 と 3、スクロール バーを置くと、そのアクションをモデル**SeekRowApprox**を呼び出すと、 _ulNumerator_と_ulDenominator_を使用して同等の小数部から成る値を渡すことによって。 **SeekRowApprox**の検索では、テーブルの先頭からの絶対常にします。 テーブルの末尾に移動するには、 _ulNumerator_と_ulDenominator_の値は同じである必要があります。 
  
適切な任意の数のスキームを使用します。 テーブルを中間の位置にシークに、1/2、10 月 20、または 50 または 100 を指定できます。 
  
## <a name="see-also"></a>関連項目



[IMAPITable : IUnknown](imapitableiunknown.md)

