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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ae2729ec5620b6b408a5c999d4b6ede7143bed2f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584567"
---
# <a name="imapiviewcontext--iunknown"></a>IMAPIViewContext : IUnknown

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
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

