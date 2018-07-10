---
title: Outlook MAPI リファレンスの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4c126d0c-d7c0-45c0-801c-c9f1e44c9db6
description: '�ŏI�X�V��: 2013�N2��1��'
ms.openlocfilehash: c0d7faaa957167977606cd93800a085d62b214f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801700"
---
# <a name="outlook-mapi-reference-overview"></a>Outlook MAPI リファレンスの概要

**適用されます**: Outlook 
  
このトピックでは、Outlook 2013 MAPI のリファレンス ドキュメントの概要情報を提供します。
  
## <a name="about-this-documentation"></a>このマニュアルについて

このドキュメントは、Microsoft Outlook 2013 でメッセージング API (MAPI) の実装に適用されます。 
  
Microsoft Office Outlook 2007 では、以前は、MAPI のプログラマーズ リファレンスは、Microsoft Exchange のドキュメントの一部をでした。
  
> [!NOTE]
> Exchange は、MAPI の使用を Microsoft Exchange Server 2007 以降 deemphasized はため、Exchange の実装が制限されているをサポートします。 
  
MAPI の Outlook の実装は、Microsoft Exchange の実装によって異なります。 Outlook の実装では、クライアント コンピューターで実行するために最適化し、低レイテンシを強調しています。 Exchange の実装は、サーバが高可用性と優れたマルチ スレッドが重要です。
  
エンド ・ ユーザーのシステムで実行するアプリケーションにこのドキュメントを使用します。 サーバー アプリケーションでは、MAPI が該当する場合の Exchange の実装を使用して、または Exchange Web サービスなど、Exchange の現在の Api を使用します。 Exchange Web サービスの詳細については、 [Exchange Web サービスの参照](http://msdn.microsoft.com/en-us/library/bb204119.aspx)を参照してください。
  
MAPI、Outlook または Exchange の実装で動作するアプリケーションを作成することができます。 など MFCMAPI は、両方のプラットフォームでうまく動作します。 実装は、多くの一般的な機能が明らかと微妙な違いがあります。 アプリケーションのすべての環境で動作する場合は、両方のプラットフォームで慎重にテストする必要があります。 このテストにより、どちらの実装を実行して、同じオペレーティング システムのインストールではサポートされていないために、2 つのシステムが必要です。
  
MAPI は MAPI ストア内のデータへの低レベルのアクセスや、トランスポート、メッセージ ストアやアドレス帳プロバイダーを構築するために適切なことに注意します。 MAPI が Outlook のビジネス ロジックをバイパスするため、ソリューションを構築するための Api を評価するとき Outlook オブジェクト モデルの使用も考慮する必要があります。 Outlook オブジェクト モデルは Outlook のビジネス ロジックをカプセル化はしますが、マルチ スレッド コード、同期プロバイダー、または Windows サービス アプリケーションには適していません。
  
このエディションに新機能に関する情報については、次のトピックを参照してください。
  
- [���̃o�[�W�����̐V�@�\���܂��B](what-s-new-in-this-edition.md)
    
- [���� Edition �Ŕp�~���ꂽ API �v�f](api-elements-deprecated-in-this-edition.md)
    
Outlook の MAPI アプリケーションの開発に慣れていない場合は、次のトピックを参照してください。
  
- [API または Outlook 2013 のためのソリューションを開発するためのテクノロジーを選択](http://msdn.microsoft.com/en-us/library/jj900714.aspx)
    
- [�悭�g����w�b�_�[ �t�@�C��](commonly-used-header-files.md)
    
- [�悭�g�p�����v���p�e�B](commonly-used-properties.md)
    
- [�悭�g�p�����I�u�W�F�N�g](commonly-used-objects.md)
    
この参照の残りの部分は、情報の次の 3 種類に分類されます。
  
- [MAPI のサンプル](mapi-samples.md)では、API のさまざまな要素と基本の MAPI プロバイダーを実装して、Outlook アイテムを作成する方法の使用を示すコード サンプルが多数に指示します。 
    
- [MAPI の概念](mapi-concepts.md)には、MAPI のアーキテクチャと概念について説明します。 
    
- [MAPI の参照](mapi-reference.md)では、関数、インターフェイス、構造体、および MAPI のプロパティに関する詳細情報を提供します。 
    
## <a name="see-also"></a>関連項目

- [Outlook �� MAPI �Q�Ƃ̎g�p��J�n���܂��B](getting-started-with-the-outlook-mapi-reference.md)
- [MAPI Samples](mapi-samples.md)
- [MAPI �̊T�O](mapi-concepts.md)
