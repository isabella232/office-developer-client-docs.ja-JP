---
title: IMAPIProgressGetMin
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.GetMin
api_type:
- COM
ms.assetid: caceddf1-0f7c-47b5-97bf-17ffe3440a6c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: cff866ce73eb6ada45a2b629a6c95c69ad189045
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587825"
---
# <a name="imapiprogressgetmin"></a>IMAPIProgress::GetMin

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
進行状況の情報が表示される [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) メソッドの最小値を返します。 
  
```cpp
HRESULT GetMin(
  ULONG FAR * lpulMin
);
```

## <a name="parameters"></a>パラメーター

 _lpulMin_
  
> [out] 操作中のアイテムの最小数へのポインターです。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 操作中のアイテムの最小数が取得されました。
    
## <a name="remarks"></a>備考

最小値は、操作の開始を数値形式で表します。 値は、進行状況の表示全体の範囲を示すために使用されるグローバルな最大値、あるいは表示の一部のみを示すのに使用されるローカル値になります。 
  
フラグ設定の値は、進行状況オブジェクトが最小値をローカルまたはグローバルと識別するかに影響します。 MAPI_TOP_LEVEL フラグが設定されている場合、最小値はグルーバルと見なされ、操作全体の進行状況の計算に使用されます。 MAPI_TOP_LEVEL が設定されている場合は、最小値はローカルと見なされます。プロバイダーは、この値を内部で使用して下位レベルのサブオブジェクトの進行状況を表示します。 ローカルの最小値は進行状況オブジェクトによって保存されますが、この最小値は **GetMin** 呼び出しを介してのみプロバイダーに返されます。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

最小値を 1 に初期化します。 サービス プロバイダーは、**IMAPIProgress::SetLimits** メソッドを呼び出してこの値をリセットできます。 **GetMin** および [IMAPIProgress](imapiprogressiunknown.md) メソッドの実装方法の詳細については、「[進行状況インジケーターの実装](implementing-a-progress-indicator.md)」を参照してください。
  
進行状況オブジェクトを呼び出す方法とタイミングの詳細については、「[進行状況インジケーターを表示する](how-to-display-a-progress-indicator.md)」を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::GetMin  <br/> |MFCMAPI は、**IMAPIProgress::GetMin** メソッドを使用して進行状況インジケーターの最小値を取得します。 制限が設定済みである場合を除き、**IMAPIProgress::SetLimits** メソッドを呼び出して 1 を返します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProgress::GetMax](imapiprogress-getmax.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[コード サンプルとしての MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[進行状況インジケーターを表示する](how-to-display-a-progress-indicator.md)
  
[進行状況インジケーターの実装](implementing-a-progress-indicator.md)

