---
title: 'title: "MAPI �t�H���_�[���\������܂��B" ms.author: v-tirob author: v-tirob manager: soliver ms.date: 3/9/2015 ms.audience: Developer ms.topic: overview ms.prod: office-online-server localization_priority: Normal api_type:'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2e1287a3-0f15-4d9a-b7ee-738fce9cd51f
description: 'COM ms.assetid: 2e1287a3-0f15-4d9a-b7ee-738fce9cd51f description: "�ŏI�X�V��: 2015�N3��9��"'
ms.openlocfilehash: b22b8641d55037d3755fc9ae32b97455223bbd12
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431940"
---
# <a name="mapi-receive-folders"></a>title: "MAPI �t�H���_�[���\������܂��B" ms.author: v-tirob author: v-tirob manager: soliver ms.date: 3/9/2015 ms.audience: Developer ms.topic: overview ms.prod: office-online-server localization_priority: Normal api_type:

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
A receive folder holds inbound messages of a particular message class. Receive folder associations can be established by clients, by the message store provider, or by MAPI. MAPI has two default receive folders: the root folder of the message store, and the Inbox folder of the interpersonal message (IPM) subtree. The root folder of the message store is the default receive folder for all interprocess communication (IPC) messages.
  
 The Inbox folder is created by MAPI for every new message store and acts as the default receive folder for the following message classes: 
  
- IPM ���b�Z�[�W �N���X�ł��B
    
- ���|�[�g�̃��b�Z�[�W �N���X�ł��B
    
- ��̏ꍇ�A�܂��͕s�����Ă���A�N���X�łł��B
    
All report messages, even those sent in response to an IPC message, are placed in the Inbox folder. IPC client applications that process their own reports must explicitly add a receive folder for the particular class of report. For example, if a client expects to receive messages with the class IPC.Paper.Order, it should call the [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) method to establish a receive folder for reports with the class Report.IPC.Paper.Order. 
  
Receive folder associations are based on the hierarchical organization of message classes. Clients can explicitly establish an association between a receive folder and a message class or use the MAPI default receive folders. Typically, clients designate one folder to receive messages for a base class and all of its subclasses. For example, a typical client would establish an association for messages with the class **MyClass**. Then if the client received messages with classes **MyClass.Home** or **MyClass.Home.Kitchen.Computer**, these messages would go to the receive folder for the base class, **MyClass**.
  
�X�g�A�g�p���@��N���C�A���g�𑀍삷��ɂ́A�t�H���_�[���\������鎟�� 3 �̃��b�Z�[�W������܂��B
  
- [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md)
    
- [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)
    
- [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md)
    
The receive folder table is a listing of information about all of the receive folders established for a message store. Its required column set includes the message class, record key, and entry identifier.
  
To retrieve a receive folder for a particular message class, clients pass the message class string to the [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) method. The message store provider returns an entry identifier for the corresponding folder. To implement **GetReceiveFolder**, a message store provider should use an algorithm that selects the folder whose associated message class matches the longest possible prefix of the specified message class. For example, assume the message store has the following associations between receive folders and message classes in its receive folder table:
  
- **IPM**���b�Z�[�W�́A��M�g���C] �t�H���_�[�Ɋi�[����܂��B 
    
- **IPM.Note.Sample**���b�Z�[�W�́A[�T���v��] �t�H���_�[�Ɋi�[����܂��B 
    
�K�؂Ȃ��܂��܂ȃN���X�Ń��b�Z�[�W��ǂ̂悤�Ƀ��[�e�B���O����A���̕\�ł́A�t�H���_�[���\������܂��B
  
|**�N���X�̃��b�Z�[�W���M���܂��B**|**�t�H���_�[���\������܂��B**|
|:-----|:-----|
|**IPM.メモ: 簡単な例** <br/> |�T���v���̃t�H���_�[  <br/> |
|**IPM.Note** <br/> |��M�g���C] �t�H���_�[  <br/> |
|**IPM.カード** <br/> |��M�g���C] �t�H���_�[  <br/> |
|**IPM.メモ. 単純な完全** <br/> |�T���v���̃t�H���_�[  <br/> |
   
Clients call the **SetReceiveFolder** method to make an explicit association between a particular message class and receive folder. When a message is delivered to an empty message class, MAPI places the message in the receive folder that is defined for a prefix of the empty class. For example, if your client has a receive folder established for messages with class **IPM** and a message with class **IPM.Note.Test** is delivered, this message will be placed in the receive folder for the **IPM** message class. 
  
**SetReceiveFolder**��Ăяo���ł́A�N���C�A���g���ʏ�̓��b�Z�[�W�̃N���X�̕������n�����A�V�����G���g�����ʎq���t�H���_�[���M���܂��B�������A�N���C�A���g�́A�����̃p�����[�^�[�̈���܂��͗����� NULL �œn�����Ƃ��ł��܂��B���̕\�ł́A���b�Z�[�W�̃N���X�ƃG���g�����ʎq�p�����[�^�[�� NULL ��w�肷�邱�Ƃ��猋�ʂ̓���ɂ��Đ�����܂��B 
  
|**_SetReceiveFolder_�p�����[�^�[**|**���ʂ̓���**|
|:-----|:-----|
|�G���g���̎��ʎq�� NULL �ɐݒ肵�܂��B  <br/> |The message store deletes the association between the specified message class and its existing receive folder. A new receive folder is not established.  <br/> ���̃��b�Z�[�W �N���X **GetReceiveFolder**�ȍ~�ł́A���b�Z�[�W �N���X�̃v���t�B�b�N�X�̎�M] �t�H���_�[��Ԃ��܂��V�������b�Z�[�W�̕ۑ��A **GetReceiveFolder**�� IPM ��A��M�g���C��Ԃ��܂��B  <br/> |
|���b�Z�[�W�̃N���X�� NULL �ɐݒ肵�܂��B  <br/> |The message store changes the association for the empty message class to the indicated folder. Incoming messages whose class is otherwise unrecognized will go to this folder.  <br/> |
|�G���g�����ʎq����у��b�Z�[�W �N���X�� NULL �ɐݒ肵�܂��B  <br/> |The message store deletes the class/folder association for the empty message class. You should not set both parameters to NULL, because it typically results in inbound messages being placed in the root folder of the message store, a folder that is invisible to the client.  <br/> |
   
���b�Z�[�W�̃N���X�͋�ɂ��Ȃ��ŁA��̃��b�Z�[�W��N���X���������邱�Ƃ��ł��܂��B���b�Z�[�W �X�g�A�̐ӔC�� **IPM**���̃N���X����V�����̑��M���b�Z�[�W�Ƀ��b�Z�[�W�̃N���X����蓖�Ă��M���b�Z�[�W�̔C�ӂ̋�̃N���X����N���X�Ƃ��� **IPM.Note**����蓖�Ă�g�����X�|�[�g �v���o�C�_�[�̒S�����邱�Ƃ�����߂��܂��B 
  
## <a name="see-also"></a>関連項目



[MAPI �t�H���_�[](mapi-folders.md)

