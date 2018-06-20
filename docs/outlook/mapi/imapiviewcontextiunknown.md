---
title: IMAPIViewContext IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext
api_type:
- COM
ms.assetid: d566ff39-92c1-4a14-85e5-1c406825f805
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a7d62253baaaae7955e722874a15d05ed16e566e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800881"
---
# <a name="imapiviewcontext--iunknown"></a>IMAPIViewContext: IUnknown

  
  
**適用されます**: Outlook 
  
クライアント アプリケーションのフォームのビューアーでフォームを管理します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform.h  <br/> |
|によって公開されます。  <br/> |コンテキスト オブジェクトの表示  <br/> |
|によって実装されます。  <br/> |フォームの閲覧者  <br/> |
|によって呼び出されます。  <br/> |フォーム オブジェクト  <br/> |
|インターフェイスの識別子。  <br/> |IID_IMAPIViewContext  <br/> |
|ポインターの型。  <br/> |LPMAPIVIEWCONTEXT  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[SetAdviseSink](imapiviewcontext-setadvisesink.md) <br/> |ビューアーの変更についての通知を受信するフォームの登録を管理します。  <br/> |
|[ActivateNext](imapiviewcontext-activatenext.md) <br/> |フォーム ビューアー内の次または前のメッセージをアクティブにします。  <br/> |
|[GetPrintSetup](imapiviewcontext-getprintsetup.md) <br/> |現在、印刷情報を取得します。  <br/> |
|[GetSaveStream](imapiviewcontext-getsavestream.md) <br/> |現在のメッセージを保存するために使用するストリームを取得します。  <br/> |
|[GetViewStatus](imapiviewcontext-getviewstatus.md) <br/> |ビューアーの現在の状態を取得します。  <br/> |
|[発生しました](imapiviewcontext-getlasterror.md) <br/> |前のビューのコンテキスト内で発生したエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)

