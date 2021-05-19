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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6a7bb7265d29d2acfce17a1a09c95f7f7b539064
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348623"
---
# <a name="itnefaddprops"></a>ITnef::AddProps

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
呼び出し元のサービス プロバイダーまたはゲートウェイが、メッセージまたは添付ファイルのカプセル化にプロパティを追加できます。 
  
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
  
> [in]カプセル化にプロパティを含めるか、カプセル化から除外する方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
TNEF_PROP_ATTACHMENTS_ONLY 
  
> メッセージの添付ファイルの一部である  _lpPropList_ パラメーターのプロパティのみをエンコードします。 
    
TNEF_PROP_CONTAINED 
  
> _ulElemID_ パラメーターで指定された添付ファイルのプロパティのみをエンコードします。 _lpvData_ パラメーターが NULL ではない場合、指すデータは **、PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) プロパティで示されるファイル内の添付ファイルのカプセル化に書き込まれます。
    
TNEF_PROP_CONTAINED_TNEF 
  
> _ulElemID_ パラメーターで指定されたメッセージまたは添付ファイルのプロパティのみをエンコードします。 このフラグが設定されている場合  _、lpvData の値は_ [IStream ポインターである必要](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) があります。 
    
TNEF_PROP_EXCLUDE 
  
> lpPropList パラメーターで指定されていないすべての  _プロパティをエンコード_ します。 
    
TNEF_PROP_INCLUDE 
  
> lpPropList で指定されたプロパティ  _をエンコードします_。 
    
TNEF_PROP_MESSAGE_ONLY 
  
> メッセージ自体の一部である  _lpPropList_ で指定されたプロパティのみをエンコードします。 
    
 _ulElemID_
  
> [in]添付ファイル **のPR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) プロパティで、親メッセージ内の添付ファイルを一意に識別する番号が含まれる。 _ulElemID パラメーター_ は、添付ファイルに対して特別な処理が要求される場合に使用されます。 _ulElemID_ パラメーターは _、ulFlags_ パラメーターで TNEF_PROP_CONTAINEDまたはTNEF_PROP_CONTAINED_TNEFフラグが設定されていない限り、0 である必要があります。 
    
 _lpvData_
  
> [in]  _ulElemID_ で指定された添付ファイルのデータを置き換えるのに使用される添付ファイル データへのポインター。 _lpvData パラメーター_ は _、ulFlags_ でTNEF_PROP_CONTAINEDまたはTNEF_PROP_CONTAINED_TNEF場合をTNEF_PROP_CONTAINED_TNEF NULL である必要があります。
    
 _lpPropList_
  
> [in]カプセル化に含める、またはカプセル化から除外するプロパティの一覧へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

トランスポート プロバイダー、メッセージ ストア プロバイダー、およびゲートウェイは **、ITnef::AddProps** メソッドを呼び出して、メッセージまたは添付ファイルの Transport-Neutral カプセル化形式 (TNEF) 処理に含まれるプロパティまたは除外されるプロパティを一覧表示します。 プロバイダーまたはゲートウェイは、連続した呼び出しを使用して、追加およびエンコードまたはエンコードから除外するプロパティの一覧を指定できます。 プロバイダーとゲートウェイは **、AddProps** を使用して、特別な処理添付ファイルに関する情報を提供することもできます。 
  
 **AddProps** は [、OpenTnefStream または OpenTnefStreamEx](opentnefstream.md) 関数の TNEF_ENCODE フラグで開いた TNEF オブジェクト [でのみサポート](opentnefstreamex.md) されます。 
  
[ITnef::Finish](itnef-finish.md)メソッドが呼び出されるまで **、AddProps** の実際の TNEF エンコードは発生しない点に注意してください。 この機能は **、AddProps** に渡されるポインターは、Finish の呼び出しが行われた後まで有効なまま **である必要があります** 。 その時点で **、AddProps** 呼び出しで渡されたオブジェクトとデータはすべて解放または解放できます。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|File.cpp  <br/> |SaveToTNEF  <br/> |MFCMAPI は **、ITnef::AddProps** メソッドを使用して、メッセージから TNEF ストリームにプロパティをコピーします。  <br/> |
   
## <a name="see-also"></a>関連項目



[ITnef::Finish](itnef-finish.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[PidTagAttachTransportName 標準プロパティ](pidtagattachtransportname-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

