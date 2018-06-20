---
title: ��M�g���C ���b�Z�[�W �X�g�A��̃t�H���_�[�����M�g���C
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8e4ce129-137d-4618-80a6-88781a578d01
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 2bd71ee4fca53fbf3d309cbaf9d33835b84c0c2d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801061"
---
# <a name="inbox-and-outbox-folders-in-message-stores"></a>��M�g���C ���b�Z�[�W �X�g�A��̃t�H���_�[�����M�g���C

  
  
**適用されます**: Outlook 
  
既定のメッセージ ストアには、メッセージ ストア プロバイダーは受信トレイを実装し、フォルダーを [送信トレイ] する必要があります。 通常メッセージ ストアの IPM サブツリーに格納されます。 これらのフォルダーは、特別な特別な機能のこれらの必要はありませんがメッセージを配信してから送信されたフォルダーとして指定されます。 クライアント アプリケーションとの間、MAPI スプーラーでは、メッセージ ストア プロバイダーの定義済みの呼び出しシーケンスを使用してメッセージの送受信が行われます。 単なるものの中にメッセージを保持するために使用されているフォルダー、受信トレイ、送信トレイ フォルダーのシーケンスを呼び出します。 重要なポイントはフォルダーは、特別なまたは受信トレイと送信トレイはその名前が偶数ではありません。重要なポイントは、メッセージ ストア プロバイダーは、そのサポートの一環としてメッセージを送受信するためです。
  
メッセージの受信をサポートするには、メッセージ ストア プロバイダーは、 [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md)メソッドと[IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)メソッドを実装しなければなりません。 詳細については、[メッセージ ストア プロバイダーを使用してメッセージの受信](receiving-messages-by-using-message-store-providers.md)を参照してください。
  
メッセージの送信をサポートするために、メッセージ ストア プロバイダーはメッセージの送信処理中に、MAPI スプーラーによって使用される他の方法だけでなく、 [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)メソッドをサポートしなければなりません。 メッセージ ストアの送信キューをメッセージ ストアのフォルダー ツリーで任意の場所の実際のフォルダーに対応する必要はありません。 ただし、いずれかを使用する必要がある場合、[送信トレイ] フォルダーで、メッセージの発信キューの内容を表示するのには、メッセージ ストア プロバイダーの慣習です。 クライアント アプリケーションにメッセージ ・ ストア内の他のすべてのフォルダーと、[送信トレイ] フォルダーを表示することができますので、ユーザーに送信すると、メッセージの状態を示すために便利な方法は、これを行います。 詳細については、[メッセージ ストア プロバイダーを使用してメッセージの送信](sending-messages-by-using-message-store-providers.md)を参照してください。
  
## <a name="see-also"></a>�֘A����



[���[���̕ۑ��ꏊ�Ńt�H���_�[��������܂��B](implementing-folders-in-message-stores.md)

