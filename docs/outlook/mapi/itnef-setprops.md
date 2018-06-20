---
title: ITnefSetProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.SetProps
api_type:
- COM
ms.assetid: 09e4b427-316b-4630-9f3d-81e74f040d7b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 480a50bd8c3738ad7d0c178cb4cabfdecd15412e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801238"
---
# <a name="itnefsetprops"></a>ITnef::SetProps

  
  
**適用されます**: Outlook 
  
元のメッセージまたは添付ファイルを変更することがなくカプセル化されたメッセージまたは添付ファイルの 1 つまたは複数のプロパティの値を設定します。 
  
```cpp
HRESULT SetProps(
  ULONG ulFlags,
  ULONG ulElemID,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]プロパティの値を設定する方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
TNEF_PROP_CONTAINED 
  
> メッセージまたは添付ファイルの_ulElemID_パラメーターで指定されたプロパティのみをエンコードします。 
    
 _ulElemID_
  
> [in]添付ファイルの**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) プロパティは、一意にその数値が含まれていますが、親メッセージの添付ファイルを識別します。
    
 _あう_
  
> [in]_LpProps_パラメーターが指す[SPropValue](spropvalue.md)構造体のプロパティ値の数です。 
    
 _lpProps_
  
> [in]設定するプロパティのプロパティ値を含む**SPropValue**構造体へのポインター。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 呼び出しが成功し、予期される値または値が返されます。
    
## <a name="remarks"></a>備考

プロバイダー、転送メッセージ ストア プロバイダーでは、プロパティを設定するのにはゲートウェイの呼び出し、 **ITnef::SetProps**メソッドに含める元のメッセージまたは添付ファイルを変更することがなく、メッセージまたは添付ファイルをカプセル化します。 この呼び出しで設定されたプロパティは、カプセル化されたメッセージ内の既存のプロパティをオーバーライドします。 
  
 **SetProps**が[OpenTnefStream](opentnefstream.md)または[OpenTnefStreamEx](opentnefstreamex.md)関数の場合、TNEF_ENCODE フラグを使用して開かれている TNEF オブジェクトに対してのみサポートされています。 プロパティの任意の数は、この呼び出しで設定できます。 
  
> [!NOTE]
> **SetProps**の実際の TNEF エンコードが行われないまで、 [ITnef::Finish](itnef-finish.md)メソッドが呼び出された後です。 **SetProps**に渡されたポインターに保つように有効期限**を終了**する呼び出しが行われた後、この機能を示します。 その時点で、すべてのオブジェクトと**SetProps**の呼び出しに渡されるデータは、リリースまたは解放されます。 
  
## <a name="see-also"></a>関連項目



[ITnef::Finish](itnef-finish.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[PidTagAttachNumber の標準的なプロパティ](pidtagattachnumber-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[ITnef: IUnknown](itnefiunknown.md)

