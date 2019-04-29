---
title: imapi進捗状況
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.Progress
api_type:
- COM
ms.assetid: edbf7623-a64e-43b8-8379-e3cde2433d91
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3cf639286a504b9edb600214d13dbe50710e76a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435496"
---
# <a name="imapiprogressprogress"></a>IMAPIProgress::Progress

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
操作が完了した時点で進行状況のインジケーターを更新します。 
  
```cpp
HRESULT Progress(
  ULONG ulValue,
  ULONG ulCount,
  ULONG ulTotal
);
```

## <a name="parameters"></a>パラメーター

 _ulvalue_
  
> 順番現在の進行状況のレベルを示す数値 ( _ulcount_および_ulcount_パラメーター、または[imapiprogress:: setlimits](imapiprogress-setlimits.md)メソッドの_l/min_および_lアウト max_パラメーターから、グローバルな間で計算されます)。下限とグローバルの上限値。 
    
 _ulcount_
  
> 順番現在処理されているアイテムを合計に対して示す数値。
    
 _ultotal_
  
> 順番操作中に処理されるアイテムの合計数。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 進行状況のインジケーターが正常に更新されました。
    
## <a name="notes-to-implementers"></a>実装に関するメモ

_ulvalue_パラメーターは、操作の開始時にのみグローバル最小値となり、操作の完了時にのみグローバル最大値に等しくなります。 
  
_ulcount_パラメーターと_ulcount_パラメーター (使用可能な場合) を使用して、"5 個のアイテムが完了しました" のようなオプションのメッセージを表示します。 _ulcount_と_ulcount_が0に設定されている場合は、進行状況インジケーターを視覚的に変更するかどうかを決定します。 一部のサービスプロバイダーでは、このパラメーターを0に設定して、進行状況が親オブジェクトに対して監視されているサブオブジェクトを処理していることを示します。 このような状況では、親オブジェクトが進捗状況を報告する場合にのみ、表示を変更することをお勧めします。 一部のサービスプロバイダーは、これらのパラメーターに対して常に0を渡します。 
  
**進行状況**およびその他の[imapiprogress](imapiprogressiunknown.md)メソッドを実装する方法の詳細については、「[進行状況インジケーターの実装](implementing-a-progress-indicator.md)」を参照してください。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**imapiprogress**の3つのパラメーターすべてではありません。:P rogress が必要です。 必須のパラメーターは_ulvalue_のみで、進行状況の割合を示す数値です。 MAPI_TOP_LEVEL フラグが設定されている場合は、オブジェクトの数と合計を渡すこともできます。 実装によっては、これらの値を使用して、進行状況のインジケーターが表示された "5 個のアイテムが10を完了しました" のような語句を表示します。 
  
すべてのメッセージを単一のフォルダーにコピーする場合は、 _ultotal_をコピーするメッセージの合計数に設定します。 フォルダーをコピーする場合は、 _ultotal_をフォルダー内のサブフォルダーの数に設定します。 コピーするフォルダーにサブフォルダーとメッセージのみが含まれている場合は、 _ultotal_を1に設定します。 
  
進行状況オブジェクトを呼び出す方法とタイミングの詳細については、「[進行状況インジケーターを表示する](how-to-display-a-progress-indicator.md)」を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |cmapiprogress 進行状況::P rogress  <br/> |mfcmapi は、 **imapiprogress::P rogvalumethod**を使用して、現在の進行状況 ( _uvalue_および現在の最大値および最小値から計算された) を使用して、mfcmapi ステータスバーを更新します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[コード サンプルとしての MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[進行状況インジケーターを表示する](how-to-display-a-progress-indicator.md)
  
[進行状況インジケーターの実装](implementing-a-progress-indicator.md)

