---
title: MAPI プロバイダーとコンポーネントの相互作用
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 2c0e010b-0432-4ef7-a243-3a4b46f0a19d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d9cec36654328accadce77a3f67da58542774aa6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564085"
---
# <a name="interaction-of-mapi-providers-and-components"></a>MAPI プロバイダーとコンポーネントの相互作用

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
任意の種類の MAPI サービス プロバイダーは、他の MAPI コンポーネントを使用するには、特定のガイドラインに従う必要があります。 各サービス プロバイダーは、次の条件を実行する必要があります。
  
- 初期化には、適切なプロバイダー オブジェクトとログオン オブジェクトを使用します。
    
- 初期化時に、プロバイダー エントリ ポイントのディスパッチ テーブルをメッセージング システムに返します。
    
- プロバイダーが所有する各リソースの MAPI 状態テーブル行を登録し、適切な時間に [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) メソッドを呼び出します。 
    
- 有効な一意識別子 (UID) を取得するには [、IMAPISupport::NewUID](imapisupport-newuid.md) メソッドを使用します。 
    
- 返されるオブジェクトの一般的な MAPI インターフェイスをサポートします。
    
- MAPI メモリ割り当て関数を使用して、クライアント アプリケーションに返されるメモリを割り当て、MAPI サブシステムの他の部分によって割り当てられたメモリを解放します。
    
- 必要に応じて、基になるメッセージング システムに資格情報を格納するプロファイル セクションを維持します。
    
- [IMAPISupport::RegisterPreprocessor メソッド](imapisupport-registerpreprocessor.md)を使用して、メッセージの前処理関数を登録します。 
    
- 共通の定数、構造、インターフェイス、および戻り値を定義する適切なヘッダー ファイル (mapispi.h を含む) を含めます。
    
- 一般的なアドレスの種類については、アドレス形式の規則に従います。
    

