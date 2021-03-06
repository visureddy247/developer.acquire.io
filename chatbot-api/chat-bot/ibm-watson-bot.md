# IBM Watson Integration

## **Getting started tutorial**

This guide will allow you to integrate the Acquire platform with IBM Watson

### **Before you begin**

A Watson service instance must be started first.

1. [Sign up](https://cloud.ibm.com/catalog/services/watson-assistant) for a free IBM Cloud account or [log in](https://cloud.ibm.com/catalog/services/watson-assistant) with your existing account.
2. Load the [Watson Assistant](https://cloud.ibm.com/catalog/services/watson-assistant) page in the IBM Cloud catalog.
3. The Watson service instance will be created in the **default** resource group. Please note if you wish to change the resource group change it at this stage as it cannot be changed later. However, this group is sufficient for the purposes of exploring the Acquire chat bot integration.
4. If you're creating an instance for production use, which is more robust, then learn more about [resource groups](https://cloud.ibm.com/docs/resources/bestpractice_rgs#bp_resourcegroups).
5. Choose an appropriate region/location to deploy your instance in.
6. Click **Create**.

![](https://lh6.googleusercontent.com/iyE2K04uuH5TDpkWxc6Cw0lLaffzn3ynwWdZRcUvnGp8kIQi41_969w0TnYGHnHE6ZqoGajnqhzzlCqfR_aU2racww4ul2GeJTJJH1WP7SU1qHSC8kMMi0dKUdHIUV2BSVeHggSN)

### **Step 1. Open Watson Assistant**

After creating a Watson Assistant service instance, the Watson Assistant dashboard will appear and allow you to **manage** it.

1. Click **Launch Watson Assistant**. If you're prompted to log in, provide your IBM Cloud credentials.

![](https://lh5.googleusercontent.com/TdOaPftw_zVtzQBXTge455XDJabcTT2k31CXRfwG7Xx0DguSKrdI47KPybDYHvF5Oq1ZLEKablpPc5f2Qgt2S_-X3eHphtR4Q2ajTJm6AADGkhCsswwQJZgSZ-MksQRa1YBfAhco)

### **Step 2. Create an assistant**

1. Click **Create assistant** to add an assistant.

![](https://lh5.googleusercontent.com/GEN_2PrCwEr0pZP-NUL9Pce-cEZiSJ46n_u2SNh8955OrbXJjFE5D4uPn8Jrp4V9UK4qbJqnZZE3UL0D8Vdq_DYCqriAL2X8ezjr9iyebLK_FZrmx5aiMsY1Kn1IQCRKaECjrx1B)

1. Click **Create assistant**.

![](https://lh3.googleusercontent.com/hyXA7Kd_RR2PFC-_rRQlcrxH1VdNYLCY9eTVtkzruNCxb95RgmNfoaDcZ8moziwSKCJGCpD28DaJyFbcJKQXbdKXiM2vO4jQ7uzRL38ApOxeg174_5f3plyEGcnuUn5-EN14yCu2)

### **Step 3. Create a dialog skill**

A dialog skill is a container for the artefacts that define the conversation flow that your assistant make use of to engage with your customers.

1. Click on your assistant tile to open the assistant.
2. Click **Add dialog** skill and **Create dialog skill**.

![](https://lh3.googleusercontent.com/kYeIrKz8stOHsPzHxFTkREKZo-1Dr0cVvMnjEEAmglnAwOc94_6Yiauzfhf8hYjJ6l2Nniq30HcW7YjsNadgkB_gcncljrzIOE7163ldLrLy5cne2t4SD4PUVFY6jKccSt0n5N1o)

You will then land on the Intents page.

### **Step 4. Add intents from a Content Catalog**

Here you can add training data, that was built by IBM Watson, as further skills by adding intents from the Contents Catalog. By giving the assistant access to the General Content Catalog it allows the Chat Bot to greet the visors and conclude conversations with them appropriately.

1. Click the **Content Catalog** tab.
2. Find **General** in the list, and then click **Add to skill**.

![](https://lh4.googleusercontent.com/NIR_ENHcUklUoq66x8G1UPYvx5TONSJbvJGksZ7gpJ4BGeyXHvKDo789mCSxuemUGMzIzSBu9w5zmmv5oFrprOoil4EoCDE2wkVkRhszXMQ6Rl82d1hM8PV-y-LwuSPoHbHGDXeL)

You successfully started to build your training data by adding pre-built content from IBM.

### **Step 5. Build a dialog**

A [dialog](https://cloud.ibm.com/docs/services/assistant?topic=assistant-dialog-overview) defines your conversation flow in the form of a logic tree. It matches intents \(what users say\) to responses \(what the bot says back\). Each node of the tree has a condition that triggers it, based on the user's input.

We'll create a simple dialog that handles the greeting and ending intents, each with a single node.

#### Adding nodes to handle intents

Now let's add nodes between the Welcome node and the Anything else node that handle our intents.

**1.** Click the More icon on the **Welcome** node, and then select **Add node below**.

**2.** In the **If assistant recognizes** field of this node, start to type \#General\_Greetings. Then, select the **\#General\_Greetings** option.

**3.** Add the response text, Good day to you!

**4.** Click ![](https://lh3.googleusercontent.com/OaAmaCA_hbERAAb-dqAgDKTOT31NiCqxSBuLYh_MBWmNJ407RJUGEjlQ1_tRIirsQW_Li6nlx2GF0m9rdE2GmnI-lM5m--Vryo6zqNwJ_8QFc9PSd3Oca93Z6vyQndxg_E9xNY-1)to close the edit view.

![](https://lh5.googleusercontent.com/eP5oIzSpg_Si18lBTmU_olFeVusb3F9-3Xv2hQyOMAe41I4C5jS2oTTFQEDXKTDerSq92NnPVUiJe28_up42_L6Oj9Eh4f-y4eIs70TNObCcbkYMHzO_Rd89LyjYrz5sV-jlz0B4)

**5.** Click the More icon on this node, and then select **Add node below** to create a peer node. In the peer node, specify \#General\_Ending in the **If assistant recognizes** field, and OK. See you later. as the response text.

![](https://lh5.googleusercontent.com/goHV-FhUVeaCvpcFBEbmpg7qAcoqaW9FBUTgShYcHIAtPR8yPgtWk825JSRHg-GsmEqCu4Lmu5k8vITp5v7ouTt75Rt4t9BBQl8KZiXl-LWahu7czPjyIYS0tK_J_8x16gsAfola)

**6.** Click ![](https://lh3.googleusercontent.com/we3BBvivTN5ACVkhGuDHA_0ywiV_LFclRdlsEGqm7RbopbsTd_ALd8TAqrcUvBMqPBBLmMxVnmIiQRk5W5f53pAtHZflsFWqNQoB_p01d9UmETO1wTytxZgoDbCSqo7O1aeHoS-Y)to close the edit view.

### **Step 6. Integrate with Acquire**

Go to the Acquire’s Bot Section. Here you will find all the available third-party chat-bots. The option to install “**IBM Watson Bot**” will be listed in the Bot Store.

![](https://lh6.googleusercontent.com/9c3y16yaxLY4vWj1-ryBd2o6FIpfylxWnbfYIhSVmQNvDBl9VCFvw3j3uoz4ntmKqEFP_h4cXPg0xin1vxAbDI43RQJA-Jy925mW02iAR0cylibqrD70l4h7aKbJbvRM6WJj9llN)

**1.** Click on the IBM Watson option from the Bot Store and a popup will be displayed. You will need a the following parameters \( “apikey” , “url” and “assistant\_id”\) to allow the chat widget to communicate with Acquire.

![](https://lh3.googleusercontent.com/HacCSXd_LuT5h6ieAYmo7KYB1opuX9ZJJGYf-8ISNRTLB1fYNTctQL_LQOPrvCmML7XhH8SzDKeOKVQrdGrUME3chjq-dyCmFME7dGrsu-y_qSx_y5HZ0MRvty7d0_tDT4JXAUKH)

**2.** To find your “**apikey**” and “**url**”, navigate to the Dashboard of [IBM Cloud](https://cloud.ibm.com/) and press on Services that is displayed. Click on the Watson service, It’ll navigate to IBM Watson Service Page. Copy your “**apikey**” and “**url**” and paste it to “**Acquire**” popup.

![](https://lh5.googleusercontent.com/jyefvpdFtE_LufCznEMb-9hqcg5VmQkfMlBgG4lSrpuqgjbsIoNdkds0yMyoSfldLfV69-LrmvLdQLcHBPSsQWOJgD3V-l3RSD3toBJxjOHhVWeTuVNJbkgG9xd_UhGDIhRGMaaQ)

**3.** To find your “**assistant\_id**”, Click on Launch Watson assistant button. It will display a list of all available assistants.

**4.** Select the "**More**" icon inside the assistant window and then click on settings.

![](https://lh5.googleusercontent.com/5ibi9AIZq7QhqUx6AvoRjlS7Kc25QIVBa-C4--OywkYaSL_WW8pWLSZ9fo3wVVh6_JvRKejqllPPQEMlU82IUjaypgNygGWZUuiPudgcJYQkee9aWXr9kf-runbTmDw-jiRjiPyG)

**5.** Click on API Details tab, Copy “**assistant\_id**” and paste it to “**Acquire**” popup window as shown below.

![](https://lh3.googleusercontent.com/82LNglHnWGdeZfXqF3arab3YGnTTkqkXq1LABJx_Y3VIUgh3FsHuB2XP_z_MvXxazvpkjuh8i0i9WRbnOznepdgqHp4-CqNgPEgTHl6NC7Wn3RwNK0BF7UBIAxDXNEGmUEy7-_kO)

**6.** The IBM Watson Chat Bot is now setup and ready to be deployed. Press the install button.

![](https://lh6.googleusercontent.com/aRfKdnROyKMgFbzWtyrSw-LNxV7VrBch_TaKqeOWHAESvTdXE8RIEoiEeGYcSqdFWCVStknAD4C8EErZwDEr8nphpCj1ZWSIklWJLHkh73nv8ChPgBHMmq_UjRpNYcg9XRRcMTge)

**7.** You can use the “**Trigger**” filters to allow the Chat Bot to engage with your customers and answer visitor questions.

![](https://lh5.googleusercontent.com/aCAiySLaqnZuF6YOF1oox8fxEM2YLy1uYEMRdXSxbZ5YFKKMSh-0l50qYkpdp9k6P37MPSvEBpCvVDIX7NzGWGZgq-RoRYtyq1bswYz6B-VxTNUky-lmE2VZa4Ky3sqcflFFWD__)

**8.** Finally, now you can navigate to your simulation page to test the new and improved Chatbot by entering the different types of questions that the system has been configured with.

![](https://lh6.googleusercontent.com/ldqqsEWZhoMwtgdSP9hAW4PIC9mxN_8Ec88TgWMXo4NDAUi1oy3ZKQnDQifK-7Niq9O8clARvHZ_7i7S90JJ1KPcrZJjF6vAKlk66I1bty8XFaO_HW50DxEG1dzku9cIoR8659P7)

