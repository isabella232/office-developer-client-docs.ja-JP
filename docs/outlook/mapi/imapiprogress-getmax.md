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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2dadad410b9aaf1401d792de373e561c29183a12
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567238"
---
# <a name="imapiprogressgetmax"></a>IMAPIProgress::GetMax

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
情報を表示する進行中の操作では、アイテムの最大数を返します。
  
```cpp
HRESULT GetMax(
  ULONG FAR * lpulMax
);
```

## <a name="parameters"></a>パラメーター

 _lpulMax_
  
> [out]操作内のアイテムの最大数へのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 操作内のアイテムの最大数を取得するとします。
    
## <a name="remarks"></a>注釈

最大値は、数値形式での操作の終了を表します。 値は、全体の進行状況表示の範囲を表すために使用、グローバルな最大値またはローカル値になっているため、画面の一部のみを表すために使用できます。 
  
フラグの設定の値は、実行中のオブジェクトは、ローカルまたはグローバルに最大の価値を理解しているかどうかに影響します。 MAPI_TOP_LEVEL フラグを設定すると最大値はグローバルと見なされ、処理全体の進行状況を計算するために使用します。 MAPI_TOP_LEVEL が設定されていないと最大値と見なされる、ローカル プロバイダーを使用して、内部的に低レベルのサブオブジェクトの進行状況を表示します。 進行中のオブジェクトは、 **GetMax**の呼び出しを使用して、プロバイダーに戻す場合にのみローカル最大値を保存します。 
  
方法の詳細については、実行中のオブジェクトへの呼び出しを行う場合は、[進行状況のインジケーターの表示](how-to-display-a-progress-indicator.md)を参照してください。
  
## <a name="notes-to-implementers"></a>実装者へのメモ

1000 の最大値を初期化します。 サービス プロバイダーは、 [IMAPIProgress::SetLimits](imapiprogress-setlimits.md)メソッドを呼び出すことによって、この値をリセットできます。 **GetMax**およびその他の[IMAPIProgress](imapiprogressiunknown.md)メソッドを実装する方法の詳細については、[進行状況のインジケーターを実装する](implementing-a-progress-indicator.md)を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::GetMax  <br/> |MFCMAPI では、 **IMAPIProgress::GetMax**メソッドを使用して、実行中のオブジェクトの最大値を取得します。 **IMAPIProgress::SetLimits**メソッドでの制限が既に設定されていない限り、1000 を返します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProgress::GetMin](imapiprogress-getmin.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[進行状況インジケーターを表示する](how-to-display-a-progress-indicator.md)
  
[進行状況インジケーターの実装](implementing-a-progress-indicator.md)

