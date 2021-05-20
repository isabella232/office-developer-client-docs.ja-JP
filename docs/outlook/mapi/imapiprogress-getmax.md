---
title: IMAPIProgressGetMax
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.GetMax
api_type:
- COM
ms.assetid: 88a910ed-b55a-4e5b-a43d-eb3ea795a70e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 64b6235151c7700a24992bc1d4394553a53c0464
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436203"
---
# <a name="imapiprogressgetmax"></a>IMAPIProgress::GetMax

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
進行状況情報が表示される操作内のアイテムの最大数を返します。
  
```cpp
HRESULT GetMax(
  ULONG FAR * lpulMax
);
```

## <a name="parameters"></a>パラメーター

 _lpulMax_
  
> [out]操作内のアイテムの最大数へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 操作内のアイテムの最大数が取得されました。
    
## <a name="remarks"></a>注釈

最大値は、操作の終了を数値形式で表します。 値は、進行状況の表示全体の範囲を示すために使用されるグローバルな最大値、あるいは表示の一部のみを示すのに使用されるローカル値になります。 
  
フラグ設定の値は、進行状況オブジェクトが最大値をローカルまたはグローバルに理解するかどうかに影響します。 このフラグMAPI_TOP_LEVEL設定すると、最大値はグローバルと見なされ、操作全体の進行状況を計算するために使用されます。 このMAPI_TOP_LEVEL設定されていない場合、最大値はローカルと見なされ、プロバイダーは内部的に使用して下位レベルのサブオブジェクトの進行状況を表示します。 Progress オブジェクトは、GetMax 呼び出しを介してプロバイダーに返すローカルの最大値 **のみを保存** します。 
  
進行状況オブジェクトを呼び出す方法とタイミングの詳細については、「[進行状況インジケーターを表示する](how-to-display-a-progress-indicator.md)」を参照してください。
  
## <a name="notes-to-implementers"></a>実装に関するメモ

最大値を 1000 に初期化します。 サービス プロバイダーは、[IMAPIProgress::SetLimits](imapiprogress-setlimits.md) メソッドを呼び出してこの値をリセットできます。 **GetMax** および他の [IMAPIProgress](imapiprogressiunknown.md)メソッドを実装する方法の詳細については、「Progress Indicator の実装 [」を参照してください](implementing-a-progress-indicator.md)。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::GetMax  <br/> |MFCMAPI は **IMAPIProgress::GetMax** メソッドを使用して、progress オブジェクトの最大値を取得します。 **IMAPIProgress::SetLimits** メソッドで制限が設定されていない限り、1000 を返します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProgress::GetMin](imapiprogress-getmin.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[コード サンプルとしての MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[進行状況インジケーターを表示する](how-to-display-a-progress-indicator.md)
  
[進行状況インジケーターの実装](implementing-a-progress-indicator.md)

