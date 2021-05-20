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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f7372830624d774fb914ae956e86a9e4476cf487
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430792"
---
# <a name="itnefsetprops"></a>ITnef::SetProps

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
元のメッセージまたは添付ファイルを変更せずに、カプセル化されたメッセージまたは添付ファイルの 1 つ以上のプロパティの値を設定します。 
  
```cpp
HRESULT SetProps(
  ULONG ulFlags,
  ULONG ulElemID,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [in]プロパティ値の設定方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
TNEF_PROP_CONTAINED 
  
> _ulElemID_ パラメーターで指定されたメッセージまたは添付ファイルのプロパティのみをエンコードします。 
    
 _ulElemID_
  
> [in]添付ファイル **のPR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) プロパティで、親メッセージ内の添付ファイルを一意に識別する番号が含まれる。
    
 _cValues_
  
> [in]_lpProps_ パラメーターが指す [SPropValue](spropvalue.md)構造体のプロパティ値の数。 
    
 _lpProps_
  
> [in]設定するプロパティのプロパティ値を含む **SPropValue** 構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しは成功し、予期される値または値を返しました。
    
## <a name="remarks"></a>注釈

トランスポート プロバイダー、メッセージ ストア プロバイダー、およびゲートウェイは **、ITnef::SetProps** メソッドを呼び出して、元のメッセージまたは添付ファイルを変更せずに、メッセージまたは添付ファイルのカプセル化に含めるプロパティを設定します。 この呼び出しで設定されたプロパティは、カプセル化されたメッセージ内の既存のプロパティを上書きします。 
  
 **SetProps** は [、OpenTnefStream または OpenTnefStreamEx](opentnefstream.md) 関数の TNEF_ENCODE フラグで開いた TNEF オブジェクトでのみ [サポート](opentnefstreamex.md) されます。 この呼び出しでは、任意の数のプロパティを設定できます。 
  
> [!NOTE]
> [ITnef::Finish](itnef-finish.md)メソッドが呼び出されるまで **、SetProps** の実際の TNEF エンコードは実行されません。 この機能は **、SetProps** に渡されるポインターは、Finish の呼び出しが行われた後まで有効なまま **である必要があります** 。 その時点で **、SetProps** 呼び出しに渡されるオブジェクトとデータはすべて解放または解放できます。 
  
## <a name="see-also"></a>関連項目



[ITnef::Finish](itnef-finish.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[PidTagAttachNumber 標準プロパティ](pidtagattachnumber-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[ITnef : IUnknown](itnefiunknown.md)

