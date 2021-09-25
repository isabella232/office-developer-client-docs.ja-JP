---
title: ITnefSetProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITnef.SetProps
api_type:
- COM
ms.assetid: 09e4b427-316b-4630-9f3d-81e74f040d7b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: beb4a8357e5170298078ea5f52b8585f28d14486
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561321"
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

