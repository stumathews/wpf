using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Data;
using System.Windows.Documents;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Imaging;
using System.Windows.Navigation;
using System.Windows.Shapes;

namespace WpfApplication1
{
    /// <summary>
    /// Interaction logic for MainWindow.xaml
    /// </summary>
    public partial class MainWindow : Window
    {
        public string FirstName { get; set; }
        public MainWindow()
        {
            InitializeComponent();
        }

        /// <summary>
        /// Handles the button submittion event by displaying a message to the user.
        /// More specifically, the message will be the user's name.
        /// </summary>
        /// <param name="sender"></param>
        /// <param name="e"></param>
        private void Submit(object sender, RoutedEventArgs e)
        {
            try {
                FirstName = txtName.Text;
                MessageBox.Show("Thank you. Your name has been saved.");
            } catch (Exception)
            {
                
                throw;
            }
            
        }
        /*
         Having a common event for a parent control is useful so that children within the parent
         * can have their common behaviour handled in a common even handler, instead of having a event handler
         * for each control for the onClick() event say.
         * This technology is called "Routed events" in WPF
         */

        private void StackPanel_Click_1(object sender, RoutedEventArgs e)
        {
            Button buttonCausedEvent = e.Source as Button; //Notice the usage of the RoutedEventArgs to get source of the event triggered.
            MessageBox.Show("This common event for stackpanel was caused by a bubbling event from " + buttonCausedEvent.ToString());
        }
    }
}
