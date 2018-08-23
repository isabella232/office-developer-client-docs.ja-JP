---
title: MAPI プロバイダーとコンポーネントの相互作用
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c0e010b-0432-4ef7-a243-3a4b46f0a19d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c81da7673d6c0c59de6992bc46362069daf71b42
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592627"
---
# <a name="interaction-of-mapi-providers-and-components"></a>MAPI プロバイダーとコンポーネントの相互作用

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
どのような種類の MAPI サービス プロバイダーは、その他の MAPI コンポーネントを操作する特定のガイドラインに従う必要があります。 各サービス プロバイダーにする必要があります。
  
- 初期化のため、適切なプロバイダー オブジェクトとログオン オブジェクトを使用します。
    
- メッセージング システムの初期化時にプロバイダーのエントリ ポイントのディスパッチ テーブルを返します。
    
- リソースごとに、プロバイダーによって所有されている MAPI の状態テーブルの行を登録し、適切な時点で、 [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md)メソッドを呼び出します。 
    
- [IMAPISupport::NewUID](imapisupport-newuid.md)メソッドを使用して、有効な一意の識別子 (Uid) を取得します。 
    
- 返すオブジェクトの一般的な MAPI インターフェイスをサポートします。
    
- MAPI のメモリ割り当て関数を使用して、クライアント アプリケーションに返されるメモリを割り当てると、MAPI サブシステムの他の部分によって割り当てられたメモリを解放します。
    
- 必要に応じて、基になるメッセージング システムに資格情報を格納するプロファイル] セクションを維持します。
    
- 関数を処理するすべてのメッセージを登録するのには、 [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md)メソッドを使用します。 
    
- 一般的な定数、構造体、インターフェイスを定義し、値を返す適切なヘッダー ファイル (mapispi.h など) が含まれます。
    
- アドレスのアドレスの種類の一般的な書体の表記規則に従います。
    

