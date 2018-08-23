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
ms.openlocfilehash: 2d37898b100398218d4f8762cdd3a16943d8f11a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801226"
---
# <a name="itnefaddprops"></a>ITnef::AddProps

  
  
**適用対象**: Outlook 
  
メッセージまたは添付ファイルをカプセル化するプロパティを追加するのには、呼び出し元のサービス プロバイダーまたはゲートウェイを有効にします。 
  
```cpp
HRESULT AddProps(
  ULONG ulFlags,
  ULONG ulElemID,
  LPVOID lpvData,
  LPSPropTagArray lpPropList
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]プロパティに含まれているまたはカプセル化から除外する方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
TNEF_PROP_ATTACHMENTS_ONLY 
  
> _LpPropList_パラメーターで、メッセージの添付ファイルの一部であるプロパティだけをエンコードします。 
    
TNEF_PROP_CONTAINED 
  
> _UlElemID_パラメーターで指定された添付ファイルのプロパティだけをエンコードします。 _LpvData_パラメーターが NULL でない場合は、 **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) のプロパティで指定されたファイルの添付ファイルのカプセル化に示されるデータが書き込まれます。
    
TNEF_PROP_CONTAINED_TNEF 
  
> メッセージまたは添付ファイルの_ulElemID_パラメーターで指定されたプロパティのみをエンコードします。 このフラグが設定されている場合、 _lpvData_の値は、 [IStream](http://msdn.microsoft.com/library/stg.istream%28Office.15%29.aspx)ポインターをする必要があります。 
    
TNEF_PROP_EXCLUDE 
  
> _LpPropList_パラメーターで指定されていないすべてのプロパティをエンコードします。 
    
TNEF_PROP_INCLUDE 
  
> _LpPropList_で指定されたすべてのプロパティをエンコードします。 
    
TNEF_PROP_MESSAGE_ONLY 
  
> プロパティのみ_lpPropList_で指定されているメッセージ自体の一部をエンコードします。 
    
 _ulElemID_
  
> [in]添付ファイルの**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) プロパティは、一意にその数値が含まれていますが、親メッセージの添付ファイルを識別します。 添付ファイルの特別な処理が要求されたときに、 _ulElemID_パラメーターが使用されます。 _UlFlags_パラメーターで TNEF_PROP_CONTAINED または TNEF_PROP_CONTAINED_TNEF のフラグが設定されていない限り、 _ulElemID_パラメーターは 0 にする必要があります。 
    
 _lpvData_
  
> [in]_UlElemID_で指定された添付ファイルのデータを置き換えるための添付ファイル データへのポインター。 _LpvData_パラメーターは、 _ulFlags_で TNEF_PROP_CONTAINED または TNEF_PROP_CONTAINED_TNEF が設定されていない限り、NULL にすることがあります。
    
 _lpPropList_
  
> [in]含めるか、カプセル化から除外するプロパティの一覧へのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>����

トランスポート プロバイダー、メッセージ ストア プロバイダー、およびゲートウェイは、リストのプロパティに含まれているか、トランスポート ニュートラル カプセル化形式 (TNEF) の処理、メッセージまたは添付ファイルから除外するに**ITnef::AddProps**メソッドを呼び出します。 連続呼び出しを使用すると、プロバイダーまたはゲートウェイを追加し、エンコード、またはエンコードの対象から除外するプロパティの一覧を指定できます。 プロバイダーおよびゲートウェイ ・ モデルの特別な処理の添付ファイルに関する情報を指定する必要がありますを提供するのに**AddProps**を使用できます。 
  
 **AddProps**は、 [OpenTnefStream](opentnefstream.md)または[OpenTnefStreamEx](opentnefstreamex.md)関数の場合、TNEF_ENCODE フラグを使用して開かれている TNEF オブジェクトでのみサポートされます。 
  
実際の TNEF エンコードが行われない**AddProps**の[ITnef::Finish](itnef-finish.md)メソッドが呼び出されるまでに注意してください。 この機能は、 **AddProps**に渡されたポインターに保つように有効期限**を終了**する呼び出しが行われた後を意味します。 その時点で、すべてのオブジェクトと**AddProps**の呼び出しで渡されるデータは、リリースまたは解放されます。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|File.cpp  <br/> |SaveToTNEF  <br/> |MFCMAPI では、 **ITnef::AddProps**メソッドを使用して、TNEF ストリームにメッセージからプロパティをコピーします。  <br/> |
   
## <a name="see-also"></a>関連項目



[ITnef::Finish](itnef-finish.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[PidTagAttachTransportName 標準プロパティ](pidtagattachtransportname-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

