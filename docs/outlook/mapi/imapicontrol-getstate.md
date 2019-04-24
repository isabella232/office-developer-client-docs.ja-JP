---
title: IMAPIControlGetState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.GetState
api_type:
- COM
ms.assetid: fb321b48-3e5f-4b99-9af0-a57b66f26a2e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f477c617533d66fc129c7192c9f86bb8a46afbb1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280281"
---
# <a name="imapicontrolgetstate"></a>IMAPIControl::GetState

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ボタンコントロールが有効であるか無効であるかを示す値を取得します。
  
```cpp
HRESULT GetState(
  ULONG ulFlags,
  ULONG FAR * lpulState
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lアウト状態_
  
> 読み上げボタンコントロールの状態を示す値へのポインター。 次のいずれかの値を返すことができます。
    
MAPI_DISABLED 
  
> [ボタン] コントロールは無効になっていて、クリックできません。 
    
MAPI_ENABLED 
  
> [ボタン] コントロールが有効になり、クリックできるようになります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> ボタンコントロールの状態が正常に取得されました。
    
## <a name="remarks"></a>解説

サービスプロバイダーは、 **IMAPIControl:: GetState**メソッドを実装して、ボタンコントロールの状態を MAPI に提供します。 ボタンが有効になっている場合は、マウスのクリックまたはキーの押すに応答することができます。 無効にすると、ボタンは淡色表示になり、マウスクリックまたはキーを押しても反応しません。 
  
**GetState**およびその他の[IMAPIControl: IUnknown](imapicontroliunknown.md)メソッドを実装する方法の詳細については、「 [Control オブジェクトの実装](control-object-implementation.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[IMAPIControl::Activate](imapicontrol-activate.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

