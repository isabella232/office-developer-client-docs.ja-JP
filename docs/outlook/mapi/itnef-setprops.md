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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315051"
---
# <a name="itnefsetprops"></a>ITnef::SetProps

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
元のメッセージまたは添付ファイルを変更せずに、カプセル化されたメッセージまたは添付ファイルの1つ以上のプロパティの値を設定します。 
  
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
  
> 順番プロパティ値の設定方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
TNEF_PROP_CONTAINED 
  
> _ulの id_パラメーターで指定されたメッセージまたは添付ファイルからのプロパティのみをエンコードします。 
    
 _ulの id_
  
> 順番添付ファイルの**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) プロパティ。親メッセージの添付ファイルを一意に識別する番号を含みます。
    
 _cvalues_
  
> 順番_lpprops_パラメーターによってポイントされている[spropvalue](spropvalue.md)構造のプロパティ値の数。 
    
 _lpprops_
  
> 順番設定するプロパティのプロパティ値を含む**spropvalue**構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しが成功し、予想される値または値が返されました。
    
## <a name="remarks"></a>解説

トランスポートプロバイダー、メッセージストアプロバイダー、ゲートウェイは、 **ITnef:: setprops**メソッドを呼び出して、元のメッセージまたは添付ファイルを変更せずに、メッセージまたは添付ファイルのカプセル化に含めるプロパティを設定します。 この呼び出しで設定されたプロパティは、カプセル化されたメッセージの既存のプロパティより優先されます。 
  
 **setprops**は、 [OpenTnefStream](opentnefstream.md)または[OpenTnefStreamEx](opentnefstreamex.md)関数の TNEF_ENCODE フラグを使用して開かれた TNEF オブジェクトに対してのみサポートされています。 この呼び出しでは、任意の数のプロパティを設定できます。 
  
> [!NOTE]
> [ITnef:: Finish](itnef-finish.md)メソッドが呼び出されるまで、 **setprops**の実際の TNEF エンコードは行われません。 この機能は、 **setprops**に渡されたポインターが、呼び出しが**完了**するまで有効なままである必要があることを意味します。 この時点で、 **setprops**呼び出しに渡されたすべてのオブジェクトとデータを解放または解放することができます。 
  
## <a name="see-also"></a>関連項目



[ITnef::Finish](itnef-finish.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[PidTagAttachNumber 標準プロパティ](pidtagattachnumber-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[ITnef : IUnknown](itnefiunknown.md)

