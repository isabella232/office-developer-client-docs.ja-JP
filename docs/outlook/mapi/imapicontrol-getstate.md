---
title: IMAPIControlGetState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIControl.GetState
api_type:
- COM
ms.assetid: fb321b48-3e5f-4b99-9af0-a57b66f26a2e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a8a24d00aa9646d52f7409c1234eac12109075f3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621011"
---
# <a name="imapicontrolgetstate"></a>IMAPIControl::GetState

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ボタン コントロールが有効か無効かを示す値を取得します。
  
```cpp
HRESULT GetState(
  ULONG ulFlags,
  ULONG FAR * lpulState
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lpulState_
  
> [out]ボタン コントロールの状態を示す値へのポインター。 次のいずれかの値を返します。
    
MAPI_DISABLED 
  
> ボタン コントロールは無効になり、クリックできません。 
    
MAPI_ENABLED 
  
> ボタン コントロールが有効で、クリックできます。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> ボタン コントロールの状態が正常に取得されました。
    
## <a name="remarks"></a>注釈

サービス プロバイダーは **、IMAPIControl::GetState** メソッドを実装して、MAPI にボタン コントロールの状態を提供します。 ボタンが有効になっている場合は、マウスのクリックまたはキーを押す操作に応答できます。 無効にすると、ボタンが淡色表示になり、マウスのクリックやキーの押しに応答しません。 
  
**GetState** および他の [IMAPIControl : IUnknown](imapicontroliunknown.md)メソッドを実装する方法の詳細については [、「Control Object Implementation 」を参照してください](control-object-implementation.md)。
  
## <a name="see-also"></a>関連項目



[IMAPIControl::Activate](imapicontrol-activate.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

