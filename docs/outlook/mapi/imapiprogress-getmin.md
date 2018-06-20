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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ab92aee6a8254a16c48352e371b711932bbe7427
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800636"
---
# <a name="imapiprogressgetmin"></a>IMAPIProgress::GetMin

  
  
**適用されます**: Outlook 
  
進捗状況の情報が表示されます、 [IMAPIProgress::SetLimits](imapiprogress-setlimits.md)メソッドでは、最小値を返します。 
  
```cpp
HRESULT GetMin(
  ULONG FAR * lpulMin
);
```

## <a name="parameters"></a>Parameters

 _lpulMin_
  
> [out]操作内のアイテムの最小数へのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 操作内のアイテムの最小数を取得するとします。
    
## <a name="remarks"></a>備考

最小値は、数値形式での操作の開始を表します。 値は、全体の進行状況表示の範囲を表すために使用、グローバルな最大値またはローカル値になっているため、画面の一部のみを表すために使用できます。 
  
フラグの設定の値は、実行中のオブジェクトは、ローカルまたはグローバルに最小値を理解しているかどうかに影響します。 MAPI_TOP_LEVEL フラグを設定すると、最小値はグローバルと見なされ、処理全体の進行状況を計算するために使用します。 MAPI_TOP_LEVEL が設定されていないと最小値は、ローカルと見なされるプロバイダーを使用して、内部的に低レベルのサブオブジェクトの進行状況を表示します。 進行中のオブジェクトは、 **GetMin**の呼び出しを使用して、プロバイダーに戻す場合にのみローカルの最小値を保存します。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

1 に最小値を初期化します。 サービス プロバイダーは、 **IMAPIProgress::SetLimits**メソッドを呼び出すことによって、この値をリセットできます。 **GetMin**およびその他の[IMAPIProgress](imapiprogressiunknown.md)メソッドを実装する方法の詳細については、[進行状況のインジケーターを実装する](implementing-a-progress-indicator.md)を参照してください。
  
方法の詳細については、実行中のオブジェクトへの呼び出しを行う場合は、[進行状況のインジケーターの表示](how-to-display-a-progress-indicator.md)を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::GetMin  <br/> |MFCMAPI では、 **IMAPIProgress::GetMin**メソッドを使用して、進行状況インジケーターの最小値を取得します。 制限は、 **IMAPIProgress::SetLimits**メソッドを呼び出すことですでに設定されている場合を除き、1 を返します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProgress::GetMax](imapiprogress-getmax.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress: IUnknown](imapiprogressiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[進行状況インジケーターを表示します。](how-to-display-a-progress-indicator.md)
  
[進行状況のインジケーターを実装します。](implementing-a-progress-indicator.md)

