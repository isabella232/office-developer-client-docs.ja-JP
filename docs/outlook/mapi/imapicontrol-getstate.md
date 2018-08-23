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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 3d45c4722b6a0200ea3937ba606da0af5c793df2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581854"
---
# <a name="imapicontrolgetstate"></a>IMAPIControl::GetState

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
ボタン コントロールを有効または無効にするかどうかを示す値を取得します。
  
```cpp
HRESULT GetState(
  ULONG ulFlags,
  ULONG FAR * lpulState
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lpulState_
  
> [out]ボタン コントロールの状態を示す値へのポインター。 次の値のいずれかが返されます。
    
MAPI_DISABLED 
  
> ボタン コントロールは無効になり、クリックすることはできません。 
    
MAPI_ENABLED 
  
> ボタン コントロールを有効にし、クリックすることができます。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> ボタン コントロールの状態が正常に取得しました。
    
## <a name="remarks"></a>注釈

サービス プロバイダーでは、MAPI をボタン コントロールの状態を提供する**IMAPIControl::GetState**メソッドを実装します。 ボタンが有効の場合は、マウス クリックやキー入力に応答できます。 無効の場合ボタンは淡色表示とマウス クリックやキー入力に応答しません。 
  
**GetState**および他の実装方法の詳細については[IMAPIControl: IUnknown](imapicontroliunknown.md)メソッドは、[コントロール オブジェクトの実装](control-object-implementation.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[IMAPIControl::Activate](imapicontrol-activate.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

