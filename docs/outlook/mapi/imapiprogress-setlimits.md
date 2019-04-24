---
title: imapi進捗の制限
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0810ed7ce20bba95c4286e6e042065c0c2d1a802
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339866"
---
# <a name="imapiprogresssetlimits"></a>IMAPIProgress::SetLimits

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
操作内の項目数の下限と上限を設定します。また、操作の進行状況に関する情報の計算方法を制御するフラグを設定します。
  
```cpp
HRESULT SetLimits(
  LPULONG lpulMin,
  LPULONG lpulMax,
  LPULONG lpulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpulMin_
  
> 順番操作中のアイテムの下限を含む変数へのポインター。
    
 _lプル最大_
  
> 順番操作中のアイテムの上限を含む変数へのポインター。
    
 _lアウトフラグ_
  
> 順番進行状況情報を計算する操作のレベルを制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_TOP_LEVEL 
  
> imapiprogress の値を使用し[ます。:P rogvalumethod](imapiprogress-progress.md)の_ulcount_および_ulcount_パラメーターは、現在処理されているアイテムとアイテムの合計数を示す、それぞれの処理の進行をインクリメントします。 このフラグが設定されている場合は、グローバルな下限と上限の値を設定する必要があります。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>解説

サービスプロバイダーは、 **imapiprogress:: setlimits**メソッドを呼び出して、MAPI_TOP_LEVEL フラグを設定またはクリアし、ローカルおよびグローバルの最小値と最大値を設定します。 flag 設定の値は、progress オブジェクトが最小値と最大値をローカルまたはグローバルに認識するかどうかに影響します。 MAPI_TOP_LEVEL フラグが設定されている場合、これらの値はグローバルと見なされ、操作全体の進行状況を計算するために使用されます。 Progress オブジェクトは、グローバルの最小値を1に、グローバルの最大値を1000に初期化します。 
  
MAPI_TOP_LEVEL が設定されていない場合、最小値と最大値はローカルと見なされ、プロバイダーはこれらを内部的に使用して、下位レベルのサブオブジェクトの進行状況を表示します。 progress オブジェクトは、 [imapiprogress:: getmin](imapiprogress-getmin.md)および[imapiprogress:: getmin](imapiprogress-getmax.md)メソッドが呼び出されたときに、プロバイダーに返されることができるように、ローカルの最小値と最大値のみを保存します。 
  
**setlimits**およびその他の[imapiprogress](imapiprogressiunknown.md)メソッドを実装する方法の詳細については、「[進行状況インジケーターの実装](implementing-a-progress-indicator.md)」を参照してください。
  
進行状況オブジェクトを呼び出す方法とタイミングの詳細については、「[進行状況インジケーターを表示する](how-to-display-a-progress-indicator.md)」を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |cmapiprogress 進行状況:: setlimits  <br/> |mfcmapi は、 **imapiprogress:: setlimits**メソッドを使用して、progress オブジェクトの最大値と最小値、およびフラグを設定します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProgress::GetMax](imapiprogress-getmax.md)
  
[IMAPIProgress::GetMin](imapiprogress-getmin.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[コード サンプルとしての MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[進行状況インジケーターを表示する](how-to-display-a-progress-indicator.md)
  
[進行状況インジケーターの実装](implementing-a-progress-indicator.md)

