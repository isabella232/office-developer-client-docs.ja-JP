---
title: IMAPIFormMgrPrepareForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.PrepareForm
api_type:
- COM
ms.assetid: 8f8ee2cb-1c2a-4958-b01e-2f4aab689f89
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 3b10ac5906be0f95930be3bef51fe2d78d583b03
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800572"
---
# <a name="imapiformmgrprepareform"></a>IMAPIFormMgr::PrepareForm

  
  
**適用対象**: Outlook 
  
開始するためのフォームをダウンロードします。
  
```cpp
HRESULT PrepareForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMINFO pfrmiInfo
);
```

## <a name="parameters"></a>パラメーター

 _ulUIParam_
  
> [in]フォームをダウンロード中に表示される進行状況のインジケーターの親ウィンドウへのハンドル。 _UlFlags_パラメーターで MAPI_DIALOG フラグが設定されていない場合、 _ulUIParam_パラメーターは無視されます。 
    
 _ulFlags_
  
> [in]フォームをダウンロードする方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_DIALOG 
  
> ステータスを指定するか、詳細についてはユーザーの入力を求めるのためのユーザー インターフェイスを表示します。 このフラグが設定されていない場合、ユーザー インターフェイスは表示されません。
    
 _pfrmiInfo_
  
> [in]ダウンロードするフォームのフォームについてはオブジェクトへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>����

フォーム ビューアーでは、開くフォームのコンテナーからフォームをダウンロードする**IMAPIFormMgr::PrepareForm**メソッドを呼び出します。 フォームのほとんどのビューアーは、 [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)と[IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md)の両方のメソッドが必要な場合は、 **PrepareForm**を呼び出すため**PrepareForm**を呼び出す必要はありません。 
  
ダイナミック リンク ライブラリ (Dll) とそれらを変更するのにはフォームに関連付けられているその他のファイルを取得するのに**PrepareForm**を使用することができます。 変更後のフォームは、フォームのコンテナーに読み込まれている場合に再インストールする必要があります。 
  
## <a name="see-also"></a>関連項目



[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

