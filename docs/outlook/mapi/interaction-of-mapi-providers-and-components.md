---
title: MAPI プロバイダーとコンポーネントの相互作用
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c0e010b-0432-4ef7-a243-3a4b46f0a19d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b88eafcc1ca6be98c5c1e9418072a5cb35f43345
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434663"
---
# <a name="interaction-of-mapi-providers-and-components"></a>MAPI プロバイダーとコンポーネントの相互作用

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
すべての種類の mapi サービスプロバイダーは、特定のガイドラインに従って他の mapi コンポーネントと連携する必要があります。 各サービスプロバイダーは次のことを行う必要があります。
  
- 適切なプロバイダーおよびログオンオブジェクトを使用して初期化を行います。
    
- 初期化時に、プロバイダーエントリポイントのディスパッチテーブルをメッセージングシステムに返します。
    
- プロバイダーが所有する各リソースに対して MAPI 状態テーブル行を登録し、 [imapisupport:: modifystatusrow](imapisupport-modifystatusrow.md)メソッドを適切な時刻に呼び出します。 
    
- 有効な一意識別子 (uid) を取得するには、 [imapisupport:: newuid](imapisupport-newuid.md)メソッドを使用します。 
    
- 返されるオブジェクトの一般的な MAPI インターフェイスをサポートします。
    
- mapi メモリ割り当て関数を使用して、クライアントアプリケーションに返されるメモリを割り当て、mapi サブシステムの他の部分によって割り当てられたメモリを解放します。
    
- 必要に応じて、基になるメッセージングシステムに資格情報を格納するために、プロファイルセクションを維持します。
    
- [imapisupport:: registerpreprocessor プロセッサ](imapisupport-registerpreprocessor.md)メソッドを使用して、任意のメッセージプリプロセス関数を登録します。 
    
- 一般的な定数、構造体、インターフェイス、および戻り値を定義する適切なヘッダーファイル (mapispi を含む) を含めます。
    
- 一般的なアドレスの種類のアドレス形式の規則に従います。
    

