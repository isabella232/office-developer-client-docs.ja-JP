---
title: IMSLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon
api_type:
- COM
ms.assetid: d87093dc-f705-465f-ab3c-944ca0cd3e54
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 991e48aa458a58ad2d7d688e81dbb357ef9bda5b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428880"
---
# <a name="imslogon--iunknown"></a>IMSLogon : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージストアのログオンオブジェクト内のリソースにアクセスします。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapispi  <br/> |
|公開者:  <br/> |メッセージストアのログオンオブジェクト  <br/> |
|実装元:  <br/> |メッセージストアプロバイダー  <br/> |
|呼び出し元:  <br/> |MAPI  <br/> |
|インターフェイス識別子:  <br/> |IID_IMSLogon  <br/> |
|ポインターの種類:  <br/> |lpmslogon  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[GetLastError](imslogon-getlasterror.md) <br/> |メッセージストアオブジェクトに対して発生した最後のエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。  <br/> |
|[Logoff](imslogon-logoff.md) <br/> |メッセージストアプロバイダーからログオフします。  <br/> |
|[OpenEntry](imslogon-openentry.md) <br/> |folder オブジェクトまたは message オブジェクトを開き、オブジェクトへのポインターを返します。これにより、さらにアクセスできるようになります。  <br/> |
|[CompareEntryIDs](imslogon-compareentryids.md) <br/> |2つのエントリ識別子を比較して、同じオブジェクトを参照しているかどうかを判断します。  <br/> |
|[助言](imslogon-advise.md) <br/> |メッセージストアの変更について通知するために、オブジェクトをメッセージストアプロバイダーに登録します。  <br/> |
|[アドバイズ](imslogon-unadvise.md) <br/> |**IMSLogon:: Advise**メソッドの呼び出しを使用して、以前に作成されたメッセージストア変更の通知用のオブジェクトの登録を削除します。  <br/> |
|[openstatusentry](imslogon-openstatusentry.md) <br/> |status オブジェクトを開きます。  <br/> |
   
## <a name="remarks"></a>注釈

メッセージストアのログオンオブジェクトは、MAPI が直接呼び出す、開いているメッセージストアプロバイダーの一部です。 MAPI が呼び出すメッセージストアのログオンオブジェクトと、クライアントアプリケーションが呼び出すメッセージストアオブジェクトとの間には、1対1の対応があります。ログオンおよびストアオブジェクトは、2つのインターフェイスを公開する1つのオブジェクトと考えることができます。 2つのオブジェクトが一緒に作成され、一緒に解放されます。
  
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

