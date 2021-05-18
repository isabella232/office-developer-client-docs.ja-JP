---
title: IMAPIProgressSetLimits
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.SetLimits
api_type:
- COM
ms.assetid: 63c9e316-ee53-4065-8154-449639643ff7
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0810ed7ce20bba95c4286e6e042065c0c2d1a802
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421467"
---
# <a name="imapiprogresssetlimits"></a>IMAPIProgress::SetLimits

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
操作のアイテム数の下限と上限、および操作の進行状況情報の計算方法を制御するフラグを設定します。
  
```cpp
HRESULT SetLimits(
  LPULONG lpulMin,
  LPULONG lpulMax,
  LPULONG lpulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpulMin_
  
> [in]操作内のアイテムの下限を含む変数へのポインター。
    
 _lpulMax_
  
> [in]操作内のアイテムの上限を含む変数へのポインター。
    
 _lpulFlags_
  
> [in]進行状況情報を計算する操作のレベルを制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_TOP_LEVEL 
  
> [IMAPIProgress::P rogress メソッド](imapiprogress-progress.md)の _ulCount_ パラメーターと _ulTotal_ パラメーターの値を使用します。これは、現在処理されているアイテムと合計アイテムをそれぞれ示し、操作の進行状況を増分します。 このフラグを設定すると、グローバル下限と上限の値を設定する必要があります。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

サービス プロバイダーは **IMAPIProgress::SetLimits** メソッドを呼び出して、MAPI_TOP_LEVEL フラグを設定またはクリアし、ローカルおよびグローバルの最小値と最大値を設定します。 フラグ設定の値は、進行状況オブジェクトがローカルまたはグローバルの最小値と最大値を理解するかどうかに影響します。 このフラグMAPI_TOP_LEVEL設定すると、これらの値はグローバルと見なされ、操作全体の進行状況を計算するために使用されます。 Progress オブジェクトは、グローバル最小値を 1 に、グローバル最大値を 1000 に初期化します。 
  
このMAPI_TOP_LEVEL設定されていない場合、最小値と最大値はローカルと見なされ、プロバイダーはそれらを内部的に使用して下位レベルのサブオブジェクトの進行状況を表示します。 Progress オブジェクトは [、IMAPIProgress::GetMin](imapiprogress-getmin.md) メソッドと [IMAPIProgress::GetMax](imapiprogress-getmax.md) メソッドが呼び出された場合にプロバイダーに返される場合にのみ、ローカルの最小値と最大値を保存します。 
  
**SetLimits** および他の [IMAPIProgress](imapiprogressiunknown.md)メソッドを実装する方法の詳細については、「Progress Indicator の実装 [」を参照してください](implementing-a-progress-indicator.md)。
  
進行状況オブジェクトを呼び出す方法とタイミングの詳細については、「[進行状況インジケーターを表示する](how-to-display-a-progress-indicator.md)」を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::SetLimits  <br/> |MFCMAPI は **IMAPIProgress::SetLimits** メソッドを使用して、進行状況オブジェクトの最大および最小の制限とフラグを設定します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProgress::GetMax](imapiprogress-getmax.md)
  
[IMAPIProgress::GetMin](imapiprogress-getmin.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[コード サンプルとしての MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[進行状況インジケーターを表示する](how-to-display-a-progress-indicator.md)
  
[進行状況インジケーターの実装](implementing-a-progress-indicator.md)

