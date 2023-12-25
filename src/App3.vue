<template>
    <div class="header">
      <PageHeaders title="Order Details" description="Let's check your store today"></PageHeaders>
      <PageSidebarMenu3></PageSidebarMenu3>
    </div>
      <!-- <div class="components"> -->
      <!-- <TextInput></TextInput>
      <EmailInput></EmailInput>  
      <PasswordInput></PasswordInput>
      <NumberInput></NumberInput>
      <FileInput></FileInput>
      <DateTime></DateTime>
      <Select></Select>
      <TextArea></TextArea>
      <CheckBox></CheckBox>
      <RadioBox></RadioBox>
      <Toggles></Toggles>
      <Button></Button>
      <DropButton></DropButton>
      <GroupButton></GroupButton>
      <Sliders></Sliders>
      <Forms></Forms>
      <InputGroups></InputGroups>
      <Card :src="Aimat"></Card>
      <Accordion></Accordion>
      <Collapse></Collapse>
      <Labels label="dad"></Labels>
      <ProgressBar value="53"></ProgressBar>
      <Tooltips text="Lorem ipsum"></Tooltips>
      <MessageBox message="message" type="dscdsv"></MessageBox>
      <Modal visible="true"></Modal>
      <Alert message="jealousy jealousy" type="success"></Alert>
      <Icons name="Arman Arman"></Icons>
      <ImageCarousel :images="images"></ImageCarousel>
      <Table :headers="headers" :rows="data"></Table>
      <List :items="items"></List>
      <PageFooters></PageFooters>
      <PageSidebarMenu title="Out of My Head" :menuItems="menu"></PageSidebarMenu>
      <Search></Search>
      <Breadcrumb :items="breadcrumb"></Breadcrumb>
      <Pagination></Pagination>
      <Tags :tags="tags"></Tags>
      <ListGroup :items="listGroup"></ListGroup>
      <NavigationLinks></NavigationLinks>
      <LinkGroups></LinkGroups>
      <Navbar></Navbar>
      <Tabs></Tabs>
      <Drawers></Drawers>
      <Spin isLoading="false"></Spin>
      <Divider height="10px" color="red"></Divider>
      <Image></Image>
      <Text></Text>
      <UserProfileImg></UserProfileImg>
      <DatePicker></DatePicker>
      <GridSystem></GridSystem>
      <Line></Line>
      <Bar></Bar>
      <Circle></Circle>
    </div> -->
  </template>
  
  <script>
    import TextInput from "./components/TextInput.vue"
    import EmailInput from "./components/EmailInput.vue"
    import PasswordInput from "./components/PasswordInput.vue"
    import NumberInput from "./components/NumberInput.vue"
    import FileInput from "./components/FileInput.vue"
    import DateTime from "./components/DateTime.vue"
    import Select from "./components/Select.vue"
    import TextArea from "./components/TextArea.vue"
    import CheckBox from "./components/CheckBox.vue"
    import RadioBox from "./components/RadioBox.vue"
    import Toggles from "./components/Toggles.vue"
    import Button from "./components/Button.vue"
    import DropButton from "./components/DropButton.vue"
    import GroupButton from "./components/GroupButton.vue"
    import Sliders from "./components/Sliders.vue"
    import Forms from "./components/Forms.vue"
    import InputGroups from "./components/InputGroups.vue"
    import Card from "./components/Card.vue"
    import Accordion from "./components/Accordion.vue"
    import Collapse from "./components/Collapse.vue"
    import Labels from "./components/Labels.vue"
    import ProgressBar from "./components/ProgressBar.vue"
    import Tooltips from "./components/Tooltips.vue"
    import MessageBox from "./components/MessageBox.vue"
    import Modal from "./components/Modal.vue"
    import Alert from "./components/Alert.vue"
    import Icons from "./components/Icons.vue"
    import ImageCarousel from "./components/ImageCarousel.vue"
    import Table from "./components/Table.vue"
    import List from "./components/List.vue"
    import PageHeaders from "./components/PageHeaders3.vue"
    import PageFooters from "./components/PageFooters.vue"
    import PageSidebarMenu3 from "./components/PageSidebarMenu3.vue"
    import Search from "./components/Search.vue"
    import Breadcrumb from "./components/Breadcrumb.vue"
    import Pagination from "./components/Pagination.vue"
    import Tags from "./components/Tags.vue"
    import ListGroup from "./components/ListGroup.vue"
    import NavigationLinks from "./components/NavigationLinks.vue"
    import LinkGroups from "./components/LinkGroups.vue"
    import Navbar from "./components/Navbar.vue"
    import Tabs from "./components/Tabs.vue"
    import Drawers from "./components/Drawers.vue"
    import Spin from "./components/Spin.vue"
    import Divider from "./components/Divider.vue"
    import Image from "./components/Image.vue"
    import Text from "./components/Text.vue"
    import UserProfileImg from "./components/UserProfileImg.vue"
    import DatePicker from "./components/DatePicker.vue"
    import GridSystem from "./components/GridSystem.vue"
    import Line from "./components/Line.vue"
    import Bar from "./components/Bar.vue"
    import Circle from "./components/Circle.vue"
  
    import Aimat from './assets/WIN_20230622_23_09_33_Pro.jpg'
    import Aimat2 from './components/assets/WIN_20231202_01_50_16_Pro.jpg'
    import Aimat3 from './components/assets/WIN_20231222_04_46_46_Pro.jpg'
    import Aimat4 from './components/assets/WIN_20231222_04_47_32_Pro.jpg'
    export default{
      components: {
      TextInput,
      EmailInput,
      PasswordInput,
      NumberInput,
      FileInput,
      DateTime,
      Select,
      TextArea,
      CheckBox,
      RadioBox,
      Toggles,
      Button,
      DropButton,
      GroupButton,
      Sliders,
      Forms,
      InputGroups,
      Card,
      Accordion,
      Collapse,
      Labels,
      ProgressBar,
      Tooltips,
      MessageBox,
      Modal,
      Alert,
      Icons,
      ImageCarousel,
      Table,
      List,
      PageHeaders,
      PageFooters,
      PageSidebarMenu3,
      Search,
      Breadcrumb,
      Pagination,
      Tags,
      ListGroup,
      NavigationLinks,
      LinkGroups,
      Navbar,
      Tabs,
      Drawers,
      Spin,
      Divider,
      Image,
      Text,
      UserProfileImg,
      DatePicker,
      GridSystem,
      Line,
      Bar,
      Circle
  },
      data(){
        return{
          Aimat,
          Aimat2,
          Aimat3,
          Aimat4,
          images:[
            Aimat2,
            Aimat3,
            Aimat4
          ],
          headers:[
            'ID',
            'Name',
            'Age'
          ],
          data:[
            ['1', 'Aimat', '18'],
            ['2', 'Arman', '-37'],
            ['3', 'Miras', '12'],
            ['4', 'Olzhas', '69']
          ],
          items:[
            "list1", "list2", 'list3'
          ],
          menu:[
            'Collide', 'Collabe'
          ],
          breadcrumb: [
          { label: 'Home', link: '/' },
          { label: 'Products', link: '/products' },
          { label: 'Category A', link: '/products/category-a' },
          { label: 'Current Page' },
          ],
          tags:[
            "One","Two","Three"
          ],
          listGroup:[
            "Option1","Option2","Option3"
          ]
        }
      }
    };
  </script>