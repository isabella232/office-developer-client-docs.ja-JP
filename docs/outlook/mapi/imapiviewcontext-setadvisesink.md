---
title: IMAPIViewContextSetAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.SetAdviseSink
api_type:
- COM
ms.assetid: 4799084a-b5d1-48c3-a889-b2f0e9d68c30
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 555bb4820dc36934fb28197b7e222633a5248125
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583184"
---
# <a name="imapiviewcontextsetadvisesink"></a>IMAPIViewContext::SetAdviseSink

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
ビューアーの変更についての通知を受信するフォームの登録を管理します。 
  
```cpp
HRESULT SetAdviseSink(
LPMAPIFORMADVISESINK pmvns
);
```

## <a name="parameters"></a>パラメーター

 _pmvns_
  
> [in]フォームへのポインターでは、シンク オブジェクトまたは NULL を案内します。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 登録またはフォームの通知の取り消しに成功しました。
    
## <a name="remarks"></a>注釈

フォーム オブジェクトは、いずれかの登録フォーム ビューアーでの変更点について説明する前の登録をキャンセルする**IMAPIViewContext::SetAdviseSink**メソッドを呼び出します。 _Pmvns_を NULL に設定すると、フォームは、登録をキャンセルしようとします。 有効なフォームに_pmvns_ポイントは、シンクをアドバイス、フォームの今後の通知を登録しようとします。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

**SetAdviseSink**にフォームが含まれていますとシンク ポインターの通知、通知をキャンセルするのには別の**SetAdviseSink**呼び出しが行われるまでは、オブジェクトへの参照を保持します。 ビューアーで、新しいメッセージをロードするときに変更が発生したときに通知を送信します。 
  
詳細については、[送信およびフォームの通知の受信](sending-and-receiving-form-notifications.md)を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::SetAdviseSink  <br/> |MFCMAPI では、この関数では、 **IMAPIViewContext::SetAdviseSink**メソッドを実装します。  <br/> |
   
## <a name="see-also"></a>関連項目



[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

