---
title: IMAPIControlActivate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.Activate
api_type:
- COM
ms.assetid: 2b641030-2429-4217-a648-0a9f3d1a1b29
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 7f330ef3099175dde88bec2de3512a3c4af1db49
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580685"
---
# <a name="imapicontrolactivate"></a>IMAPIControl::Activate

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
ダイアログ ボックスを表示する、クライアント アプリケーションのユーザーは、ボタン コントロールをクリックすると、プログラムの操作を開始するなどのタスクを実行します。
  
```cpp
HRESULT Activate(
  ULONG ulFlags,
  ULONG_PTR ulUIParam
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _ulUIParam_
  
> [in]ボタン コントロールを表示するダイアログ ボックスの親ウィンドウへのハンドル。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> ボタン コントロールが正常にアクティブ化します。
    
## <a name="remarks"></a>注釈

**IMAPIControl::Activate**メソッドでは、次のボタン コントロールのクリックをユーザーのタスクを実行します。 、表示された表の処理の一部として、クリックが発生した MAPI 後ボタンが有効になっているかどうかを決定する最初の呼び出し[IMAPIControl::GetState](imapicontrol-getstate.md) **をアクティブにする**呼び出しが行われます。 
  
**アクティブにして**、その他の実装方法の詳細については[IMAPIControl: IUnknown](imapicontroliunknown.md)メソッドは、[コントロール オブジェクトの実装](control-object-implementation.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[IMAPIControl::GetState](imapicontrol-getstate.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

