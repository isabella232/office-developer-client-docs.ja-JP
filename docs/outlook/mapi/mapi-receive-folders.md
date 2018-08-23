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
ms.openlocfilehash: 619bd2d5e3b40e49da835d774035ba237af06699
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801424"
---
# <a name="mapi-receive-folders"></a>MAPI �t�H���_�[���\������܂��B

  
  
**適用対象**: Outlook 
  
受信フォルダーは、特定のメッセージ クラスの受信メッセージを保持します。 クライアントによって、メッセージ ストア プロバイダー、または MAPI の関連付けを確立することができますフォルダーが表示されます。 MAPI には、2 つの既定のフォルダーが表示されます: メッセージ ・ ストアのルート フォルダーと、個人間メッセージ (IPM) サブツリーの [受信トレイ] フォルダー。 メッセージ ・ ストアのルート フォルダーは、既定のフォルダーのすべてのプロセス間通信 (IPC) メッセージを受信します。
  
 MAPI によってすべての新しいメッセージ ストアの受信トレイ フォルダーが作成され、次のメッセージ クラスのフォルダーが表示される既定値としての役割を果たします。 
  
- IPM ���b�Z�[�W �N���X�ł��B
    
- ���|�[�g�̃��b�Z�[�W �N���X�ł��B
    
- ��̏ꍇ�A�܂��͕s�����Ă���A�N���X�łł��B
    
IPC メッセージに対する応答として送信されたものであっても、すべてのレポート メッセージは、受信トレイ フォルダーに配置されます。 独自のレポートを処理する IPC クライアント アプリケーションでは、レポートの特定のクラスの受信フォルダーを明示的に追加する必要があります。 IPC クラスにメッセージを受信するクライアントが要求している場合などです。Paper.Order、その Report.IPC.Paper.Order のクラスを使ったレポートの受信フォルダーを確立するために[IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md)メソッドを呼び出す必要があります。 
  
メッセージ クラスの階層構造に基づく関連のフォルダーが表示されます。 クライアントは、明示的に受信フォルダーとメッセージ クラス間の関連付けを確立または MAPI の既定の受信フォルダーを使用できます。 通常、クライアントは、基本クラスのメッセージを受信する 1 つのフォルダーとそのすべてのサブクラスを指定します。 などの標準的なクライアントは、 **MyClass**クラスにメッセージをアソシエーションを確立すると。 クライアントは、 **MyClass.Home**または**MyClass.Home.Kitchen.Computer**のクラスでメッセージを受信する場合これらのメッセージは、基本クラス**MyClass**の受信フォルダーに移動します。
  
�X�g�A�g�p���@��N���C�A���g�𑀍삷��ɂ́A�t�H���_�[���\������鎟�� 3 �̃��b�Z�[�W������܂��B
  
- [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md)
    
- [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)
    
- [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md)
    
受信フォルダーのテーブルは、すべてのメッセージ ・ ストアに対して設定されている受信フォルダーに関する情報の一覧です。 必要な列のセットには、メッセージ クラス、レコード、およびエントリの識別子が含まれています。
  
受信フォルダーを特定のメッセージ クラスを取得するためには、クライアントは、メッセージ クラスの文字列を[IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)メソッドに渡します。 メッセージは、プロバイダーを返します。 対応するフォルダーのエントリ id を格納します。 **GetReceiveFolder**を実装するには、メッセージ ストア プロバイダーは、関連付けられているメッセージ クラスが指定したメッセージ クラスの可能な最長のプレフィックスに一致するフォルダーを選択するアルゴリズムを使用してください。 たとえば、メッセージ ・ ストアには、次の関連付けの間でフォルダーが表示され、メッセージ内のクラスのフォルダーのテーブルが表示されます。
  
- **IPM**���b�Z�[�W�́A��M�g���C] �t�H���_�[�Ɋi�[����܂��B 
    
- **IPM.Note.Sample**���b�Z�[�W�́A[�T���v��] �t�H���_�[�Ɋi�[����܂��B 
    
�K�؂Ȃ��܂��܂ȃN���X�Ń��b�Z�[�W��ǂ̂悤�Ƀ��[�e�B���O����A���̕\�ł́A�t�H���_�[���\������܂��B
  
|**�N���X�̃��b�Z�[�W���M���܂��B**|**�t�H���_�[���\������܂��B**|
|:-----|:-----|
|**IPM.Note.Sample.Simple** <br/> |�T���v���̃t�H���_�[  <br/> |
|**IPM.Note** <br/> |��M�g���C] �t�H���_�[  <br/> |
|**IPM.タイムカード** <br/> |��M�g���C] �t�H���_�[  <br/> |
|**IPM.Note.Sample.Simple.Totally** <br/> |�T���v���̃t�H���_�[  <br/> |
   
クライアントは、特定のメッセージ クラスとの間の明示的な関連付けを作成し、フォルダーを表示する**SetReceiveFolder**メソッドを呼び出します。 空のメッセージ クラスにメッセージを配信すると、MAPI は、空のクラスのプレフィックスで定義されている受信フォルダーにメッセージを配置します。 など、クライアントがメッセージに設定されている受信フォルダーを持っている場合クラス**IPM**とメッセージ クラス IPM を**とします。Note.Test**が配信される場合、このメッセージは、 **IPM**メッセージ クラスの受信フォルダーにします。 
  
**SetReceiveFolder**��Ăяo���ł́A�N���C�A���g���ʏ�̓��b�Z�[�W�̃N���X�̕������n�����A�V�����G���g�����ʎq���t�H���_�[���M���܂��B�������A�N���C�A���g�́A�����̃p�����[�^�[�̈���܂��͗����� NULL �œn�����Ƃ��ł��܂��B���̕\�ł́A���b�Z�[�W�̃N���X�ƃG���g�����ʎq�p�����[�^�[�� NULL ��w�肷�邱�Ƃ��猋�ʂ̓���ɂ��Đ�����܂��B 
  
|**_SetReceiveFolder_�p�����[�^�[**|**���ʂ̓���**|
|:-----|:-----|
|�G���g���̎��ʎq�� NULL �ɐݒ肵�܂��B  <br/> |メッセージ ・ ストアの指定の間の関連付けを削除するメッセージのクラスと、既存のフォルダーが表示されます。 新しい受信フォルダーが確立されていません。  <br/> ���̃��b�Z�[�W �N���X **GetReceiveFolder**�ȍ~�ł́A���b�Z�[�W �N���X�̃v���t�B�b�N�X�̎�M] �t�H���_�[��Ԃ��܂��V�������b�Z�[�W�̕ۑ��A **GetReceiveFolder**�� IPM ��A��M�g���C��Ԃ��܂��B  <br/> |
|���b�Z�[�W�̃N���X�� NULL �ɐݒ肵�܂��B  <br/> |メッセージ ・ ストアでは、指定されたフォルダーに空のメッセージ クラスとの関連付けを変更します。 クラスが認識されていませんそれ以外の場合、受信メッセージは、このフォルダーに送られます。  <br/> |
|�G���g�����ʎq����у��b�Z�[�W �N���X�� NULL �ɐݒ肵�܂��B  <br/> |メッセージ ・ ストアでは、空のメッセージ クラスとクラス] の [フォルダーの関連付けを削除します。 通常の受信メッセージのメッセージ ・ ストアは、クライアントに表示されないフォルダーのルート フォルダーに置かれる結果となるために NULL の場合、両方のパラメーターを設定する必要がありますできません。  <br/> |
   
���b�Z�[�W�̃N���X�͋�ɂ��Ȃ��ŁA��̃��b�Z�[�W��N���X���������邱�Ƃ��ł��܂��B���b�Z�[�W �X�g�A�̐ӔC�� **IPM**���̃N���X����V�����̑��M���b�Z�[�W�Ƀ��b�Z�[�W�̃N���X����蓖�Ă��M���b�Z�[�W�̔C�ӂ̋�̃N���X����N���X�Ƃ��� **IPM.Note**����蓖�Ă�g�����X�|�[�g �v���o�C�_�[�̒S�����邱�Ƃ�����߂��܂��B 
  
## <a name="see-also"></a>�֘A����



[MAPI �t�H���_�[](mapi-folders.md)

