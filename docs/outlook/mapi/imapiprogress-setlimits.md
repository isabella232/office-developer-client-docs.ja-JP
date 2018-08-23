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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 010f69b70324d4280a34d2fe06d670e07d922d86
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586775"
---
# <a name="imapiprogresssetlimits"></a>IMAPIProgress::SetLimits

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
操作、および操作の進行状況の情報を計算する方法を制御するフラグでは、アイテム数の上限と下限の制限を設定します。
  
```cpp
HRESULT SetLimits(
  LPULONG lpulMin,
  LPULONG lpulMax,
  LPULONG lpulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpulMin_
  
> [in]操作内の項目の最小値を含む変数へのポインター。
    
 _lpulMax_
  
> [in]操作内の項目の最大値を含む変数へのポインター。
    
 _lpulFlags_
  
> [in]進捗状況の情報を計算する操作のレベルを制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_TOP_LEVEL 
  
> [IMAPIProgress::Progress](imapiprogress-progress.md)メソッドの_ulCount_および_ulTotal_パラメーターで、操作の進行状況をインクリメント、それぞれ、現在処理済みのアイテムとアイテムの合計を示す値を使用します。 このフラグを設定すると、グローバルの上限と下限の制限の値を設定する必要があります。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>����

サービス プロバイダーは、ローカルおよびグローバルの最小値と最大値を設定して、MAPI_TOP_LEVEL フラグを設定または**IMAPIProgress::SetLimits**メソッドを呼び出します。 フラグの設定の値は、実行中のオブジェクトは、最小値と最大値は、ローカルまたはグローバルを理解しているかどうかに影響します。 MAPI_TOP_LEVEL フラグを設定すると、これらの値はグローバルと見なされ、全体の操作の進行状況を計算するために使用します。 進行中のオブジェクトでは、グローバルの最小値を 1 と 1000 のグローバル最大値を初期化します。 
  
MAPI_TOP_LEVEL が設定されていない場合、最小値と最大値は、ローカルと見なされます、プロバイダーに内部的に使用して低レベルのサブオブジェクトの進行状況を表示します。 進行中のオブジェクトは、 [IMAPIProgress::GetMin](imapiprogress-getmin.md)メソッドと[IMAPIProgress::GetMax](imapiprogress-getmax.md)メソッドが呼び出されたときにプロバイダーに返すことができますようにするためだけにローカルの最小値と最大値を保存します。 
  
**SetLimits**およびその他の[IMAPIProgress](imapiprogressiunknown.md)メソッドを実装する方法の詳細については、[進行状況のインジケーターを実装する](implementing-a-progress-indicator.md)を参照してください。
  
方法の詳細については、実行中のオブジェクトへの呼び出しを行う場合は、[進行状況のインジケーターの表示](how-to-display-a-progress-indicator.md)を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::SetLimits  <br/> |MFCMAPI では、 **IMAPIProgress::SetLimits**メソッドを使用して、上限と下限と進行中のオブジェクトのフラグを設定します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProgress::GetMax](imapiprogress-getmax.md)
  
[IMAPIProgress::GetMin](imapiprogress-getmin.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[進行状況インジケーターを表示する](how-to-display-a-progress-indicator.md)
  
[進行状況インジケーターの実装](implementing-a-progress-indicator.md)

