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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3fc72f008d1c2610de3c74762aabc6231dabbfbd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589057"
---
# <a name="imapiprogressprogress"></a>IMAPIProgress::Progress

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
加えられると、操作の完了までの進捗状況の表示と進行状況のインジケーターが更新されます。 
  
```cpp
HRESULT Progress(
  ULONG ulValue,
  ULONG ulCount,
  ULONG ulTotal
);
```

## <a name="parameters"></a>パラメーター

 _ulValue_
  
> [in]グローバル間 ( _ulCount_および_ulTotal_パラメーターとは、 _lpulMin_と_lpulMax_メソッドのパラメーター、 [IMAPIProgress::SetLimits](imapiprogress-setlimits.md)から計算) を実行中の現在のレベルを示す数値下限値と上限にはグローバルです。 
    
 _ulCount_
  
> [in]現在処理されて項目の合計を示す数値です。
    
 _ulTotal_
  
> [in]操作中に処理する品目の合計数です。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 進行状況インジケーターが正常に更新されました。
    
## <a name="notes-to-implementers"></a>実装者へのメモ

_UlValue_パラメーターは、グローバルの最小値、操作の開始時だけにし、操作の完了時にのみグローバルの最大値に等しくなります。 
  
「5 アイテム 10 個が完了した」などのオプションのメッセージを表示するのには、利用可能な場合、 _ulCount_および_ulTotal_パラメーターを使用してください。 _UlCount_と_ulTotal_は、0 に設定されている場合は、進行状況を視覚的に変更するかどうかを決定します。 サービス プロバイダーによっては、サブオブジェクトの進行状況は、親オブジェクトを基準にして処理することを示すために 0 にこれらのパラメーターを設定します。 このような状況は、親オブジェクトの進行状況を報告する場合にのみ、表示を変更します。 サービス プロバイダーによっては、毎回これらのパラメーターに 0 を渡します。 
  
**進行状況**およびその他の[IMAPIProgress](imapiprogressiunknown.md)メソッドを実装する方法の詳細については、[進行状況のインジケーターを実装する](implementing-a-progress-indicator.md)を参照してください。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**IMAPIProgress::Progress**のパラメーターのすべての 3 つが必要です。 必要な唯一のパラメーターは、 _ulValue_、進行状況の割合を示す数値です。 MAPI_TOP_LEVEL フラグが設定されている場合は、オブジェクト数と、オブジェクトの合計も渡すことができます。 いくつかの実装では、進行状況インジケーターを 5 アイテム 10 個の完了] などの語句を表示するのにこれらの値を使用します。 
  
1 つのフォルダー内のすべてのメッセージをコピーする場合は、コピーされるメッセージの合計数に_ulTotal_を設定します。 フォルダーをコピーする場合は、フォルダー内のサブフォルダーの数に_ulTotal_を設定します。 コピーするフォルダーが含まれていないメッセージのみのサブフォルダーと、 _ulTotal_が 1 に設定します。 
  
方法の詳細については、実行中のオブジェクトへの呼び出しを行う場合は、[進行状況のインジケーターの表示](how-to-display-a-progress-indicator.md)を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::Progress  <br/> |MFCMAPI では、 **IMAPIProgress::Progress**メソッドを使用して、 _uValue_と現在の最大値と最小値から計算される、進行中の現在の割合で MFCMAPI ステータス バーを更新します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[進行状況インジケーターを表示する](how-to-display-a-progress-indicator.md)
  
[進行状況インジケーターの実装](implementing-a-progress-indicator.md)

