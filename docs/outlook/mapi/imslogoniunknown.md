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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 42e2633ac6d534be2c75c47b24c1da5ed9771e18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801056"
---
# <a name="imslogon--iunknown"></a>IMSLogon: IUnknown

  
  
**適用されます**: Outlook 
  
メッセージへのアクセスのリソースでは、ログオン オブジェクトを格納します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapispi.h  <br/> |
|によって公開されます。  <br/> |メッセージ ストアのログオン オブジェクト  <br/> |
|によって実装されます。  <br/> |メッセージ ストア プロバイダー  <br/> |
|によって呼び出されます。  <br/> |MAPI  <br/> |
|インターフェイスの識別子。  <br/> |IID_IMSLogon  <br/> |
|ポインターの型。  <br/> |LPMSLOGON  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[発生しました](imslogon-getlasterror.md) <br/> |メッセージ ストアのオブジェクトに対して発生した最後のエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。  <br/> |
|[Logoff](imslogon-logoff.md) <br/> |メッセージをログでは、プロバイダーを格納します。  <br/> |
|[OpenEntry](imslogon-openentry.md) <br/> |フォルダーまたはメッセージのオブジェクトを開くし、さらにアクセスを提供するオブジェクトへのポインターを返します。  <br/> |
|[CompareEntryIDs](imslogon-compareentryids.md) <br/> |同じオブジェクトを参照しているかどうかを決定する 2 つのエントリ id を比較します。  <br/> |
|[アドバイス](imslogon-advise.md) <br/> |メッセージ ・ ストア内の変更についての通知のメッセージ ストア プロバイダー オブジェクトに登録します。  <br/> |
|[アドバイズ中止します。](imslogon-unadvise.md) <br/> |**IMSLogon::Advise**メソッドへの呼び出しを使用して、以前に確立されたメッセージ ストアの変更を通知するためのオブジェクトの登録を削除します。  <br/> |
|[OpenStatusEntry](imslogon-openstatusentry.md) <br/> |状態オブジェクトを開きます。  <br/> |
   
## <a name="remarks"></a>備考

メッセージ ストアのログオン オブジェクトは、MAPI を直接呼び出す、開いているメッセージ ストア プロバイダーの一部です。 MAPI 呼び出しとメッセージは、クライアント アプリケーションは、次の呼び出しはオブジェクトを格納するメッセージ ストア ログオン オブジェクトが 1 対 1 対応ログオンと思われるし、2 つのインターフェイスを公開する 1 つのオブジェクトとしてオブジェクトを格納できます。 2 つのオブジェクトは、同時解放と連携して作成されます。
  
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)
