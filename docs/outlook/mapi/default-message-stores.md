---
title: ����̃��[���̕ۑ��ꏊ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: efa178eb-feb2-443f-8f6b-2ea53a456bf2
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: cece19329460b382be724faa9f0f522831cc197c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799871"
---
# <a name="default-message-stores"></a>����̃��[���̕ۑ��ꏊ

  
  
**適用対象**: Outlook 
  
既定のメッセージ ストアは、いずれかの一般的な目的のタスクをメッセージングのクライアント アプリケーションを使用できます。 いくつかのメッセージ ストア プロバイダーは、既定のメッセージ ストアとして使用する場合に必要になるメッセージ ストア プロバイダーの省略可能な機能があります。 これは、とおりです。
  
- 実装の特別なフォルダー: 受信トレイ、送信トレイ、および検索結果のフォルダーです。
    
- �J���� nonread �̃��|�[�g��񋟂��܂��B
    
- ���M����є��M�������b�Z�[�W�̑��M������܂��B
    
- �N���X�̔C�ӂ̃��b�Z�[�W����b�Z�[�W�̍쐬������܂��B
    
- ���O�t���ƕ����l�̃v���p�e�B��T�|�[�g���܂��B
    
- メッセージ ストア プロバイダーは、トランスポート プロバイダーと密接に関連があって、 [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)メソッドをサポートします。 
    
- �֘A����R���e���c�̃e�[�u����T�|�[�g���܂��B�ڍׂɂ��ẮA [�e�[�u���ȓ�e](contents-tables.md)��Q�Ƃ��Ă��������B
    
- ���M���b�Z�[�W�Ƀ��b�Z�[�W������ꍇ�ɁAMAPI �X�v�[���[�̒ʒm��T�|�[�g���܂��B
    
## <a name="see-also"></a>�֘A����



[MAPI ���b�Z�[�W �X�g�A �v���o�C�_�[�̊J��](developing-a-mapi-message-store-provider.md)

