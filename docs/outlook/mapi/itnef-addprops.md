---
title: ITnefAddProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.AddProps
api_type:
- COM
ms.assetid: e85641fb-6d3c-494a-981c-01781c7bf5bb
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6a7bb7265d29d2acfce17a1a09c95f7f7b539064
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348623"
---
# <a name="itnefaddprops"></a>ITnef::AddProps

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
呼び出し元のサービスプロバイダーまたはゲートウェイが、メッセージまたは添付ファイルのカプセル化にプロパティを追加できるようにします。 
  
```cpp
HRESULT AddProps(
  ULONG ulFlags,
  ULONG ulElemID,
  LPVOID lpvData,
  LPSPropTagArray lpPropList
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 順番カプセル化に対してプロパティを含めるか除外するかを制御するフラグのビットマスク。 次のフラグを設定できます。
    
TNEF_PROP_ATTACHMENTS_ONLY 
  
> メッセージ内の添付ファイルの一部である_lpproplist_パラメーターのプロパティのみをエンコードします。 
    
TNEF_PROP_CONTAINED 
  
> _ulの id_パラメーターで指定された添付ファイルからのみ、プロパティをエンコードします。 _lpvdata_パラメーターが NULL でない場合、指定されたデータは、 **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) プロパティによって示されるファイルの添付ファイルのカプセル化に書き込まれます。
    
TNEF_PROP_CONTAINED_TNEF 
  
> _ulの id_パラメーターで指定されたメッセージまたは添付ファイルからのプロパティのみをエンコードします。 このフラグが設定されている場合、 _lpvdata_の値は[IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream)ポインターである必要があります。 
    
TNEF_PROP_EXCLUDE 
  
> _lpproplist_パラメーターで指定されていないすべてのプロパティをエンコードします。 
    
TNEF_PROP_INCLUDE 
  
> _lpproplist_で指定されたすべてのプロパティをエンコードします。 
    
TNEF_PROP_MESSAGE_ONLY 
  
> メッセージ自体の一部である_lpproplist_で指定されたプロパティのみをエンコードします。 
    
 _ulの id_
  
> 順番添付ファイルの**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) プロパティ。親メッセージの添付ファイルを一意に識別する番号を含みます。 _ulの id_パラメーターは、添付ファイルに対して特別な処理が要求された場合に使用されます。 ulflags パラメーターに TNEF_PROP_CONTAINED または TNEF_PROP_CONTAINED_TNEF フラグが設定されていない場合、 __ _ulの id_パラメーターは0である必要があります。 
    
 _lpvdata_
  
> 順番_ulの id_で指定された添付ファイルのデータの置換に使用される添付ファイルデータへのポインター。 _lpvdata_パラメーターは、TNEF_PROP_CONTAINED または TNEF_PROP_CONTAINED_TNEF が_ulflags_で設定されていない限り、NULL である必要があります。
    
 _lpproplist_
  
> 順番カプセル化に含める、またはカプセル化から除外するプロパティのリストへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>解説

トランスポートプロバイダー、メッセージストアプロバイダー、ゲートウェイは、 **ITnef:: addprops**メソッドを呼び出して、メッセージまたは添付ファイルのトランスポートニュートラルカプセル化形式 (TNEF) の処理に含めるか、除外するプロパティを一覧表示します。 連続呼び出しを使用することにより、プロバイダーまたはゲートウェイは、追加およびエンコードするプロパティのリストを指定したり、エンコードから除外したりすることができます。 プロバイダーとゲートウェイでは、 **addprops**を使用して、特別な処理添付ファイルに関する情報を指定することもできます。 
  
 **addprops**は、 [OpenTnefStream](opentnefstream.md)または[OpenTnefStreamEx](opentnefstreamex.md)関数の TNEF_ENCODE フラグを使用して開かれた TNEF オブジェクトに対してのみサポートされます。 
  
[ITnef:: Finish](itnef-finish.md)メソッドが呼び出されるまで、 **addprops**では実際の TNEF エンコードは行われません。 この機能は、 **addprops**に渡されるポインターが、呼び出しが**完了**するまで有効なままである必要があることを意味します。 この時点で、 **addprops**呼び出しを使用して渡されたすべてのオブジェクトとデータを解放または解放することができます。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|ファイル .cpp  <br/> |SaveToTNEF  <br/> |mfcmapi は、 **ITnef:: addprops**メソッドを使用して、メッセージから TNEF ストリームにプロパティをコピーします。  <br/> |
   
## <a name="see-also"></a>関連項目



[ITnef::Finish](itnef-finish.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[PidTagAttachTransportName 標準プロパティ](pidtagattachtransportname-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

