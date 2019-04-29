---
title: imapiviewcontext IUnknown
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: db0c375218755c3a28475e2ebce2d097fb789f75
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406032"
---
# <a name="imapiviewcontext--iunknown"></a>IMAPIViewContext : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントアプリケーションのフォームビューアーでフォームを管理します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform  <br/> |
|公開者:  <br/> |コンテキストオブジェクトを表示する  <br/> |
|実装元:  <br/> |フォームビューアー  <br/> |
|呼び出し元:  <br/> |フォーム オブジェクト  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIViewContext  <br/> |
|ポインターの種類:  <br/> |LPMAPIVIEWCONTEXT  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[SetAdviseSink](imapiviewcontext-setadvisesink.md) <br/> |フォームの登録を管理して、閲覧者の変更に関する通知を受信します。  <br/> |
|[ActivateNext](imapiviewcontext-activatenext.md) <br/> |フォームビューアーで次または前のメッセージをアクティブにします。  <br/> |
|[getprintsetup](imapiviewcontext-getprintsetup.md) <br/> |現在の印刷情報を取得します。  <br/> |
|[GetSaveStream](imapiviewcontext-getsavestream.md) <br/> |現在のメッセージを保存するために使用するストリームを取得します。  <br/> |
|[getviewstatus](imapiviewcontext-getviewstatus.md) <br/> |現在のビューアーの状態を取得します。  <br/> |
|[GetLastError](imapiviewcontext-getlasterror.md) <br/> |ビューコンテキストオブジェクトで発生した前のエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

