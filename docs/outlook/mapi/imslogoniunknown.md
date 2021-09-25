---
title: IMSLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMSLogon
api_type:
- COM
ms.assetid: d87093dc-f705-465f-ab3c-944ca0cd3e54
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 732832ffba273f174cb107d8b749d7f5c3eb8187
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579790"
---
# <a name="imslogon--iunknown"></a>IMSLogon : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ ストア ログオン オブジェクト内のリソースにアクセスします。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapispi.h  <br/> |
|次のユーザーによって公開されます。  <br/> |メッセージ ストアログオン オブジェクト  <br/> |
|実装元:  <br/> |メッセージ ストア プロバイダー  <br/> |
|呼び出し元:  <br/> |MAPI  <br/> |
|インターフェイス識別子:  <br/> |IID_IMSLogon  <br/> |
|ポインターの種類:  <br/> |LPMSLOGON  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[GetLastError](imslogon-getlasterror.md) <br/> |メッセージ ストア オブジェクト [に対して](mapierror.md) 発生した最後のエラーに関する情報を含む MAPIERROR 構造体を返します。  <br/> |
|[Logoff](imslogon-logoff.md) <br/> |メッセージ ストア プロバイダーをログオフします。  <br/> |
|[OpenEntry](imslogon-openentry.md) <br/> |フォルダーまたはメッセージ オブジェクトを開き、オブジェクトへのポインターを返して、さらにアクセスできます。  <br/> |
|[CompareEntryIDs](imslogon-compareentryids.md) <br/> |2 つのエントリ識別子を比較して、同じオブジェクトを参照するかどうかを判断します。  <br/> |
|[アドバイス](imslogon-advise.md) <br/> |メッセージ ストア内の変更に関する通知のために、メッセージ ストア プロバイダーにオブジェクトを登録します。  <br/> |
|[Unadvise](imslogon-unadvise.md) <br/> |**IMSLogon::Advise** メソッドの呼び出しを使用して、以前に確立されたメッセージ ストアの変更の通知に対するオブジェクトの登録を削除します。  <br/> |
|[OpenStatusEntry](imslogon-openstatusentry.md) <br/> |状態オブジェクトを開きます。  <br/> |
   
## <a name="remarks"></a>注釈

メッセージ ストア ログオン オブジェクトは、MAPI が直接呼び出す開いているメッセージ ストア プロバイダーの一部です。 MAPI が呼び出すメッセージ ストア ログオン オブジェクトと、クライアント アプリケーションが呼び出すメッセージ ストア オブジェクトとの間には、1 対 1 の対応があります。ログオンオブジェクトとストア オブジェクトは、2 つのインターフェイスを公開する 1 つのオブジェクトと考えて使用できます。 2 つのオブジェクトは一緒に作成され、一緒に解放されます。
  
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

