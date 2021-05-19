---
title: IMAPIProgressProgress
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
  
進行状況インジケーターを更新し、操作の完了に向けて進行状況を表示します。 
  
```cpp
HRESULT Progress(
  ULONG ulValue,
  ULONG ulCount,
  ULONG ulTotal
);
```

## <a name="parameters"></a>パラメーター

 _ulValue_
  
> [in]グローバル下限とグローバル上限の間の現在の進行状況レベル _(ulCount_ パラメーターと _ulTotal_ パラメーター、[または IMAPIProgress::SetLimits](imapiprogress-setlimits.md)メソッドの _lpulMin_ パラメーターおよび _lpulMax_ パラメーターから計算) を示す数値。 
    
 _ulCount_
  
> [in]合計を基準に現在処理されているアイテムを示す数値。
    
 _ulTotal_
  
> [in]操作中に処理されるアイテムの総数。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 進行状況インジケーターが正常に更新されました。
    
## <a name="notes-to-implementers"></a>実装に関するメモ

_ulValue_ パラメーターは、操作の開始時点でのみグローバル最小値、および操作の完了時にのみグローバル最大値に等しくなります。 
  
_ulCount パラメーターと_ _ulTotal_ パラメーター (使用可能な場合) を使用して、オプションのメッセージ ("10 から 5 アイテムが完了しました" など) を表示します。 _ulCount と_ _ulTotal_ が 0 に設定されている場合は、進行状況インジケーターを視覚的に変更するかどうかを決定します。 一部のサービス プロバイダーは、親オブジェクトに対して進行状況を監視するサブオブジェクトを処理している場合に、これらのパラメーターを 0 に設定します。 このような場合は、親オブジェクトが進行状況を報告した場合にのみ表示を変更する必要があります。 一部のサービス プロバイダーは、これらのパラメーターに対して毎回 0 を渡します。 
  
**Progress** および他の [IMAPIProgress](imapiprogressiunknown.md)メソッドを実装する方法の詳細については、「Progress Indicator の実装 [」を参照してください](implementing-a-progress-indicator.md)。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**IMAPIProgress::P 3** つのパラメーターすべてが必須ではありません。 必要なパラメーターは  _ulValue_ のみで、進行状況の割合を示す数値です。 このフラグMAPI_TOP_LEVEL設定されている場合は、オブジェクト数とオブジェクトの合計を渡す方法も指定できます。 一部の実装では、これらの値を使用して、進行状況インジケーターと一緒に "10 から 5 アイテムが完了しました" などの語句を表示します。 
  
1 つのフォルダー内のすべてのメッセージをコピーする場合は  _、ulTotal_ をコピーするメッセージの総数に設定します。 フォルダーをコピーする場合は、フォルダー内のサブフォルダーの数に  _ulTotal_ を設定します。 コピーするフォルダーにサブフォルダーとメッセージだけが含まれている場合は  _、ulTotal を_ 1 に設定します。 
  
進行状況オブジェクトを呼び出す方法とタイミングの詳細については、「[進行状況インジケーターを表示する](how-to-display-a-progress-indicator.md)」を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::P rogress  <br/> |MFCMAPI は **IMAPIProgress::P rogress** メソッドを使用して  _、uValue_ および現在の最大値と最小値から計算された現在の進捗率で MFCMAPI ステータス バーを更新します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[コード サンプルとしての MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[進行状況インジケーターを表示する](how-to-display-a-progress-indicator.md)
  
[進行状況インジケーターの実装](implementing-a-progress-indicator.md)

