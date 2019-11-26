# HW5-510

## Order of steps to run the ansible playbook:

## Using baker, by spinning a vm on the localhost:

1. Go to the directory containing the baker script and the playbook files.
2. Run `baker bake`
3. Run `baker run roles`
4. Run `baker run install`

The app will be running at localhost:8080

## Without baker, on some other machine

Requirements: The host should have ansible installed.

1. Go to the directory containing the playbook scripts.
2. Update the inventory file to add the ip addresses of the machines.
2. Run `ansible-playbook roles.yml -i inventory`
3. Run `ansible-playbook main.yml -i inventory`

The app will be running on port 8080.

## Link to the screen cast: https://youtu.be/o-2RXOChZHs

## Concepts
1. Explain continuous integration. How is it used on a project?

   Continuous Integration (CI) is a development practice that requires developers to integrate code into a shared        repository, atleast daily. Each check-in is then verified by an automated build, allowing teams to detect problems early. By integrating regularly, errors can be quickly detected and located more easily. It is found that this approach leads to significantly reduced integration problems and allows a team to develop cohesive software more rapidly. By following the follwing workflow, it could be incorporated on any project.
    - Maintain a code repository
    - Automate the build
    - Make the build self-testing
    - Daily commits to the baseline by everyone on the team
    - Every commit (to the baseline) should be built
    - Make the build process fast
    - Clone the production environment for testing
    - Make it easy to get the latest deliverables
    - Everyone on the team should be able to see the results of the latest build
    - Automate build deployment

  2. Why should developers use configuration management tools to manage their software programs? What can go wrong if they don't?
  
     Configuration management is important and developers should use it because of the following benefits it offers:
       - Reduced risk of outages and security breaches through visibility and tracking of the changes to the systems.
       - Cost reduction by having detailed knowledge of all the elements of the system configuration, avoiding wasteful duplication of the technology assets.
       - Improved experience for the customers and internal staff  by rapidly detecting and correcting improper configurations that could negatively impact performance.
       - Strict control of the processes by defining and enforcing formal policies and procedures that govern asset identification, status monitoring, and auditing.
       - Greater agility and faster problem resolution, thereby enabling to provide a higher quality of service and reduce software engineering costs
       - Efficient change management by knowing the baseline configuration, and having the visibility to design changes that avoid problems.
       - Quicker restoration of service. In an outage, recovering quickly is possible as the configuration is documented and automated.
       - Better release management and clear status accounting
       
     If they dont choose to do configuration management, then the following things can go wrong:
       - Manual effort (months) to determine which system components should change when requirements change
       - Failed implementations because the project's requirements changed, and it wasn't communicated properly to all parties.
       - Lost productivity by replacing system components with flawed new versions, without the ability to quickly revert to a working state.
       - Unexpected outages from incorrectly modifying system components, because of not being able to accurately determine which components were impacted by a change.
  
